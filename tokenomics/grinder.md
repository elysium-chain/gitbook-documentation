---
description: The main Elysium Tokenomics mechanism
---

# ⚙ Grinder

The Elysium Grinder is essentially an automated central bank through which both RAY and SKY tokens are issued.

<figure><img src="../.gitbook/assets/Elysium Tokenomics.jpg" alt=""><figcaption><p>Elysium Tokenomics</p></figcaption></figure>

## RAY Supply

The Grinder controls the issuance of the RAY token to reach the target supply volume set by a mathematical formula. Since the RAY token is inflationary and the commissions paid in RAY burn, there is a constant need to create new RAY tokens. To achieve this, Grinder needs to do two tasks.

#### Grinder needs to determine the number of RAY tokens in circulation and calculate the required issuance of RAY tokens during the current day.

The mathematical formula defines the target supply depending on the day after the launch:

$$
S\left(d\right)=\frac{43500000\cdot d^{\frac{1}{8}}}{1+590e^{-\frac{d}{100}}}-40000
$$

To get the current number of tokens in circulation, Grinder must track the total number of RAYs issued and burned as commission. And given these numbers, it can calculate the certain quantity of RAYs for issuance:

$$
RAY_{circulating}\;=\;RAY_{issued}\;-\;RAY_{burned}\\RAY_{issuance}\;=\;S(d)\;-\;RAY_{circulating}
$$

#### Grinder needs to issue the required amount of RAY tokens using offers from the SKY burn order queue.

Grinder needs SKY tokens to issue RAY. There is a queue of orders arranged by the SKY / RAY rate for this purpose. The more SKYs are offered for burn in exchange for a single RAY, the sooner the Grinder will process that order. Exchange limit orders for selling are the closest analogy for such a queue. These sell limit orders are executed by a permanent purchasing volume from the Grinder.

During the order processing, one part of the SKY burns irretrievably, and the other part becomes available for reissue into circulation. The burned part equals the fraction of remaining SKY in circulation relative to the original 100 000 000. It will stop being burned when only 1 000 000 SKYs remain.

## SKY Supply

The Grinder uses a virtual SKY system pool to issue SKY. The Grinder can only take SKY from there to the extent of the burned commissions. SKY used but not burned during RAY minting returns to this virtual pool. Thus, over time, fewer and fewer SKY will be issued as a reward.

#### Issuing SKY in exchange for burned commissions.

You can imagine - that there is a virtual AMM in Grinder with a pool of (RAY burned via commissions) / (SKY for issuance). But the calculation of the SKY issue is done without having a real AMM - just by the constant product formula:

$$
SKY_{circulating}=\frac{10^{15}}{RAY_{burned}+10^7}
$$

The rate at which SKY is taken from the pool to reward validators does not directly depend on the market SKY / RAY rate. The more RAYs are burned as fees - the less SKY is issued. Thus, the volume of SKY issuance will decrease gradually.

#### Rewarding validators with SKY

The Grinder issues SKY according to the amount of burned commissions and issues it to validators as a reward. Since validator rewards are not directly dependent on the specific transactions they process, the distribution of SKY among validators can be adjusted based on many factors. In addition, this approach prevents front-running.
