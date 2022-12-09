---
description: Transaction fees are paid by users in RAY
---

# ⛽ Transaction fees

RAY will be used to pay transaction fees in the Elysium blockchain. The fee cost will depend on the total number of transactions in the network: the more transactions - the cheaper each will be.

The maximum commission in the absence of transactions will be 1 RAY, but with the growth of the activity in the network, it could fall to thousandths of a RAY.

<figure><img src="../../.gitbook/assets/Fees.jpg" alt=""><figcaption></figcaption></figure>

#### First 1000 days

The fee will be calculated according to the formula:

$$
FEE=\frac{10\;000\;000}{TXNs+10\;000\;000}
$$

#### After the first 1000 days

The fee will be calculated depending on the amount of RAY in circulation so that the limit of how much RAY can be burned in a day is 10% of its total supply:

$$
FEE=\frac{0.1\ast RAY_{supply}}{TXNs+0.1\ast RAY_{supply}}
$$





