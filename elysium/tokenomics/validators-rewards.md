---
description: Rewards are paid to validators in SKY
---

# 💰 Validators' rewards

The issuance of SKY tokens for rewarding validators comes at the expense of the burned commission in RAY and is calculated by the formula:

$$
Rewards_{total}\;=\;\frac{10^{15}}{Fees_{total}+10^7}
$$

Thus, to calculate the total award to validators for a given period, we need to take the amount of fee burned at the beginning and end of the period:

$$
Rewards_n\;=\;\frac{10^{15}}{Fees_{n-1}+10^7}-\frac{10^{15}}{Fees_n+10^7}
$$

For example if at the beginning of the day the amount of accumulated burned fee was 200 000 000 and during the day 5 000 000 of additional RAY was paid as commission, then the total reward for validators in SKY will equal:

$$
Rewards\;=\;\frac{10^{15}}{2\ast10^8+10^7}-\frac{10^{15}}{2.05\ast10^8+10^7}=4761905-4651163=110742\;SKY
$$

<figure><img src="../../.gitbook/assets/SKY issuance.jpg" alt=""><figcaption><p>How many SKY will be issued for 1000 burned RAY depending on the total amount of burned fees</p></figcaption></figure>

Rewards can be spread among specific validators according to flexible rules (e.g., depending on the percentage of time online).

It should be noted that the internal price at which SKY is issued to replace the burned RAY via commissions can be quite different from the market rate SKY / RAY. But in the long run, the two rates will tend to each other. If the inner Grinder rate is much higher than the market rate, relatively little new SKY will come into circulation, and since it will be used at a high pace to issue RAY (because of the low price) after some time, there will be a shortage of SKY at that price. If the SKY price exceeds the Grinder's issue price by a lot, the validators will have enough of it to lower the rate in the market.
