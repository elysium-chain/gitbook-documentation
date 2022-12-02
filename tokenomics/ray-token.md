# 🪙 RAY Token

## Specifications

| Parameter        | Value                                          |
| ---------------- | ---------------------------------------------- |
| Supply           | Limited by formula                             |
| Initial supply   | 100 000 000 RAYs during the first 1000 days    |
| Inflation target | \~2-3% per year after 1000 days                |
| Issuance         | Anyone can issue RAY by burning SKY in Grinder |
| Burn             | All RAYs used to pay commissions are burned    |
| Utility          | Transaction fees in Elysium are paid in RAY    |

<figure><img src="../.gitbook/assets/RAY Supply.jpg" alt=""><figcaption><p>RAY supply curve</p></figcaption></figure>

## Idea behind RAY

The RAY tokenomics should lead to an adequate commission size relative to the real world by inflation targeting. If token inflation matches real-world inflation, only the flow of money between Elysium and the outside world will affect the relative commission cost in the long run.

In the future, the RAY supply control mechanism may adjust the issuance to increase or decrease RAY inflation through one of two mechanisms: DAO or algorithmic adjustment to a basket of leading fiat currencies.

The DAO - using the subjective estimates of its participants - will be able to adjust the value of RAY relative to the real world on long time intervals by changing the slope of the RAY emission curve. The Elysium community will decide whether to establish a DAO and how it should function. But with the DAO approach, there is an apparent conflict of interest between validators (who benefit from expensive RAY) and users (who benefit from minimal fees).&#x20;

On the other hand, there are technical issues with algorithmic adjustment to the basket of leading fiat currencies. Reliable Oracles are needed to implement such an approach. But still, the system will always be at risk of an attack through external data manipulations.

But none of these approaches may be needed at all. In Elysium, another factor affects the amount of commission - the daily number of transactions. And the more transactions, the cheaper will be one transaction in RAY (for more details, read the section [Transaction fees](../elysium/tokenomics/transaction-fees.md)). There is a chance that spreading the fee over many users will balance the cost of using the system and rewards to validators.

But there is no rush - this problem will arise no sooner than 5 years after the launch of Elysium.
