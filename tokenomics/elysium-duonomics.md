---
description: Uniting the interests of system participants
---

# 🪙 Elysium Duonomics

An ideal tokenomics should facilitate the coincidence of the interests of three groups of participants:&#x20;

* Long-term holders who, having invested once, may not return to the blockchain for years.
* Regular users of the system who constantly use it for a variety of tasks.
* Validators who spend computing resources and time to keep the system running.

The coincidence of interests is not just a theoretical concept. When applied to tokenomics, it means that the growth of some functional parameter of the system must benefit all participants. Since Elysium is a truly scalable blockchain, we chose network activity, in other words, the number of transactions per unit of time, as such a parameter.&#x20;

Also, we are pretty sure that it is impossible to create a single-coin tokenomics model in which transaction growth results in gains for all participants, so Elysium tokenomics uses two coins: RAY and SKY. Their supply is managed by Elysium Grinder, which is essentially an automated central bank.

<figure><img src="../.gitbook/assets/Elysium Tokenomics.png" alt=""><figcaption><p>Elysium Tokenomics</p></figcaption></figure>

### RAY Coin

| Parameter          | Value                                              |
| ------------------ | -------------------------------------------------- |
| Maximum Supply     | Unlimited                                          |
| Circulating Supply | Limited by formula                                 |
| Initial Supply     | 1 000 000 000 RAYs during the first 1000 days      |
| Inflation          | 5% yearly after 1000 days                          |
| Utility            | Transaction fees in Elysium are paid in RAY        |
| Issuance           | Anyone can issue RAY by burning SKY in the Grinder |
| Burning            | All RAYs used to pay commissions are burned        |

What matters most to blockchain users is that transaction fees do not become very expensive. In modern blockchains, the commission amount is determined on an auction basis - the more commission users pay, the faster their transaction will be processed. This leads to two problems: frontrunning and higher fees during activity spikes.&#x20;

{% hint style="info" %}
Frontrunning is the ability to outrun someone else's massive transaction by increasing the commission paid and earning from the resulting price increase.
{% endhint %}

In Elysium, the RAY coin will be used to pay commissions. The maximum commission cost will be a fixed amount of 1 RAY, but with the growth of the network activity, the transaction cost will decrease - down to thousandths of a RAY. Moreover, because RAY is an inflationary coin with a 5% supply growth per year, its price will correlate with the real-world inflation rate in the long run.

An activity expansion is usually accompanied by coin price growth. Thus, with the increase in network activity, the relative price of RAY will grow, but the absolute value of the transaction cost expressed in RAY will decrease. This will allow the fees to remain at an acceptable level relative to the real world even at the peak of the bull run.

#### RAY Utility

All transaction fees paid in RAY are immediately burned. The base fee rate per transaction is 1 RAY. But since the volume of transactions can be large, too many RAYs can be burned in a short period. Therefore, as the number of transactions increases, the fee is reduced so that no more than 1% of the total RAY supply is burned daily.

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/Transaction fee.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The formula defines the target fee cost in RAY depending on the total number of transactions. For the first 1000 days, the formula is:

$$
Fee=\frac{10^7}{10^7+TXN_{daily}}
$$

After 1000 days the formula changes to account for the RAY inflation:

$$
Fee=\frac{0.01\ast RAY_{supply}}{0.01\ast RAY_{supply}+TXN_{daily}}
$$
{% endtab %}
{% endtabs %}

#### RAY Issuance

RAY can only be released into circulation by burning SKY in the Elysium Grinder. There is a queue of orders arranged by the SKY / RAY rate for this purpose. The more SKYs are offered in exchange for a single RAY, the sooner the Grinder will process that order. The closest analogy to such a queue is exchange limit sell orders, executed by persistent demand from the Grinder.

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/RAY Issuance.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The mathematical formula defines the RAY issuance depending on the day after the launch. For the first 1000 days, the formula is:

$$
RAY_{issuance}=52209083\cdot\frac{e^{-0.00591626\cdot x}}{\left(1+e^{-0.00591626\cdot x}\right)^{9.6}}
$$

After 1000 days the formula changes to keep the constant inflation rate:

$$
RAY_{issuance}=\frac{10^7}{73}\\
$$

These calculations apply only to newly created RAYs. Simultaneously with the issuance, RAYs will be minted through Grinder to replace the burned commission.
{% endtab %}
{% endtabs %}

#### RAY Circulating Supply

The Elysium Grinder controls the issuance of the RAY coin to reach the target circulating supply determined by a mathematical formula. Since the RAY coin is inflationary and the commissions paid in RAY are burned, there is a constant need to create new RAYs. Elysium Grinder will print RAYs providing the necessary issuance and replacing burned RAY coins to reach the target RAY circulating supply.

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/RAY Supply.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The mathematical formula defines the target supply depending on the day after the launch. For the first 1000 days, the formula is:

$$
RAY_{supply}=10^{9.0112}\cdot\left(1+e^{-0.0059162\cdot day}\right)^{-8.6}\;-\frac{10^{9.0112}}{2^{8.6}}
$$

After 1000 days the formula changes to keep the constant inflation rate:

$$
RAY_{supply}=\frac{10^7}{73}\cdot\left(day+6300\right)
$$
{% endtab %}
{% endtabs %}

### SKY Coin

| Parameter      | Value                                      |
| -------------- | ------------------------------------------ |
| Maximum Supply | 100 000 000 SKYs                           |
| Utility        | SKY is used to issue RAY                   |
| Issuance       | Can be minted only as validator's reward   |
| Burning        | A part of SKY while minting RAY is burned  |

It is vital for investors and validators that there are explicit mechanics for the growth of the asset in the long run. But in most modern networks, it is not entirely obvious what a coin is secured with, so the main criteria for long-term investments remain the limited supply of the token and the possible popularity of the decentralized system in the future.

In Elysium, SKY is designed for investment purposes and is directly secured by user activity. SKY is a RAY coin printing certificate. Its main properties are a constant demand from the system and persistent burning. Thus, the more RAY coins are burned as transaction fees, the more must be printed, and the more SKYs will be used for this purpose, part of which will be burned.

Thus, even a constant amount of daily transactions will reduce the overall supply of SKY. Therefore, both investors and validators benefit from the network activity since it directly reduces the SKY coin supply.

#### SKY Utility

SKY is used by Grinder for RAY issuance. Anyone can put SKY coins in the Grinder specifying SKY / RAY rate. The Grinder continuously uses the SKYs offers with the highest bids to issue RAYs. During the order processing, one part of the SKY burns irretrievably, and the other part becomes available for reissue into circulation. It will stop being burned when only 1 000 000 SKYs remain.

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/SKY burning.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The percantage of SKY burned depends on the amount of SKYs put in Grinder for RAY issuance. The formula is:

$$
SKY_{\%burned}\;=\;100\cdot\frac{SKY_{grindered}}{SKY_{grindered}+10^7}
$$

When the number of SKYs used for RAY issuance exeeds 990 000 000 there will remain only 1 000 000 of SKY coins and they will stop burning.
{% endtab %}
{% endtabs %}

#### **SKY Issuance**

Validators' rewards will be calculated in RAY as the sum of burned commissions and inflationary RAY issuance. SKY will be issued corresponding to that amount using a constant product formula as validators' rewards. This means that the reduction of SKY token issuance will not occur in leaps and bounds, as in the case of Bitcoin halvings, but gradually.

Since validator rewards are not directly dependent on the specific transactions they process, the distribution of SKY among validators can be adjusted based on many factors. In addition, this approach prevents front-running.

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/SKY Issuance.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The SKY supply depends on the number of RAYs minted by the Grinder. That includes all newly minted RAYs (issuance and replacement for burned coins). The number of SKYs to mint is defined by the formula:

$$
SKY_{issued}=\frac{10^{16}}{RAY_{minted}+10^8}
$$

The Grinder uses a virtual SKY system pool to issue SKY. The Grinder can only take SKY from there to the extent of the burned commissions and inflation issuance. SKY used but not burned during RAY minting returns to this virtual pool. Thus, over time, fewer and fewer SKY will be issued as a reward.

You can imagine - that there is a virtual AMM in Grinder with a pool of **RAY totally minted** / **SKY for issuance**. But the calculation of the SKY issue is done without having a real AMM - just by the constant product formula.
{% endtab %}
{% endtabs %}

#### SKY Circulating Supply

The amount of SKY circulating supply depends on the ratio of the SKY burning speed to the issuance volume. The SKY burning pace is determined primarily by the SKY market price. The SKY issuance depends on the number of RAYs burned as commissions. Thus, the exact amount of SKY in circulation can only be approximated.

Our simulation shows that though the total supply of SKY is 100 000 000, it is unlikely that there will be more than 20 000 000 SKYs in circulation at any given moment.

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/SKY Circulating Supply.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The circulating supply of SKY is calculated based on a computer model.&#x20;

It assumes that the number of transactions grows from 0 to a given number within about half a year, and the rate at which Grinder uses SKY is directly proportional to the ratio of RAY and SKY coins in circulation.
{% endtab %}
{% endtabs %}

#### RAY / SKY Rate

The RAY / SKY rate depends very much on the initial distribution of coins - therefore, it can even fall during the first few years if the number of transactions is not very high. But in the long term, the amount of RAY in circulation will grow, and the amount of SKY will fall after the peak is passed. So, in the long run, depending on the number of transactions in the blockchain, the amount of RAY given per SKY will steadily grow.

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/RAY SKY rate.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The RAY / SKY rate is calculated based on a computer model as a ratio of the RAY circulating supply and the SKY circulating supply.&#x20;

The model assumes that the number of transactions grows from 0 to a given number within about half a year, and the rate at which Grinder uses SKY is directly proportional to the ratio of RAY and SKY coins in circulation.
{% endtab %}
{% endtabs %}

|   |
| - |

## FAQ

### Do you have two tokens? But LUNA also did, and it collapsed!

If some single-token system goes bankrupt, it doesn't mean all single-token mechanics are doomed. We have fundamentally different mechanics from LUNA, self-sufficient and not directly tied to the real world. Thus, it cannot be broken by external manipulation, as it happened with LUNA.

### How will I be able to deposit or withdraw money from Elysium?

In the beginning, a bridge with Ethereum will be set up to interact with the outside world, allowing users to use wrapped ETH in Elysium. It will also be possible to withdraw capital from the Elysium network using this bridge.&#x20;

Bridges to other popular blockchains will be created in the future. If necessary, it will be possible to make a bridge with reverse logic, where RAY or SKY is withdrawn from Elysium, and in another blockchain, the user receives wrapped RAY or SKY tokens.

### What happens if no one puts SKY in the Grinder?

That won't happen. At least, the Elysium Team will put a single SKY in the Grinder queue at a price sufficient to issue a billion RAYs. And we have no doubt that there will be many such overpriced orders.

### SKY will not be burned when trading on the exchanges. Will it break the system?

There will be DEX in Elysium, so it will be possible to trade SKY for RAY outside the Grinder.&#x20;

If the price of SKY on DEX drops much relative to prices in the Grinder queue, it will open up an arbitrage opportunity. Anyone can buy a cheap SKY on the exchange and put it into the Grinder at a much higher price.&#x20;

If the price on the exchange exceeds the price in the Grinder, it would be more profitable to cancel the Grinder's order in the queue and sell the SKY on the market.&#x20;

Thus, the price on the exchange and in the Grinder queue will strongly correlate. But the burn price in the Grinder will likely be slightly higher than the exchange rate since it will take some time to process the order via the Grinder. In other words, if there is a possibility to swap SKY on the DEX immediately or through Grinder, say, within a week, then, obviously, the long wait must be somehow compensated.

### What happens if SKY collapses?

As has already been said, the prices in the Grinder queue and on the exchange correlate. If the price of SKY falls (relative to RAY), then the Grinder will start to consume (and burn) significantly more SKY. Therefore, at moments of deep SKY drawdowns, it will be burned at an accelerated pace.

### Where will the first RAY tokens come from?

The initial RAY tokens must appear somehow to launch the system. Otherwise, it will be impossible to make any transactions. For that, Elysium will have a rule (both initially and in the future) that each new validator will receive 100 RAY as a gift.

### Will SKY be distributed evenly?

SKY will be distributed among validators as a reward. Since we plan to launch a network with about a thousand initial validators, and about 10% of the total SKY supply will be distributed among them in the first year, there should be no large SKY holders.&#x20;

Well, except for the Elysium Team, which needs a lot of tokens to create bridges, provide liquidity for centralized exchanges, offer grants for developers, etc. The additional reward the Team will receive as Routers' rewards by operating the network layer.
