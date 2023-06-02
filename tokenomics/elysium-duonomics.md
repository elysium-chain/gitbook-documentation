---
description: Uniting the interests of system participants
---

# 🪙 Duonomics

## One currency is not enough

<figure><img src="../.gitbook/assets/Real world Economicsx2.png" alt=""><figcaption><p>Real-world economics</p></figcaption></figure>

Blockchain can be seen as a system that provides a service for its customers to store data in a decentralized manner. The commission for user transactions acts as payment for the work of nodes. Unlike the real world, where prices are set in fiat currencies, fees for the blockchain service are paid in coins stored within the system. But what kind of changes does this entail?

{% hint style="info" %}
If a cryptocurrency has its own blockchain, it is called a coin, unlike tokens, whose operations are processed by third-party blockchains. Thus, the description of the mechanics of how the blockchain economic model works should be called "coinomics."
{% endhint %}

The most common tokenomics model today is the one applied 13 years ago for Bitcoin. It implies that the number of coins is limited, and their issuance, which decreases over time to zero, comes as a reward to network nodes for making the system work. Therefore, users must buy them from node owners, often with fiat currency, to interact with the system.

<figure><img src="../.gitbook/assets/Standart Tokenomics.png" alt=""><figcaption><p>The most popular blockchain tokenomics</p></figcaption></figure>

It appears that users still pay nodes of the system in fiat currency but through an intermediate medium in the form of a blockchain coin. This payment arrangement has one indisputable advantage - because the number of coins is limited - when the system's popularity grows, its price skyrockets. But this same property also entails internal contradictions.

### Investments vs Coin Backing

As we already wrote in the [Positioning ](../introduction/positioning.md)section, Bitcoin is primarily a bank, and therefore, its main task is to safeguard the Bitcoins in users' accounts. So transactions can be thought of as depositing or withdrawing funds. With this approach, there is nothing wrong with a transaction taking an hour to process because the Bitcoin blockchain is not primarily a payment system.

In this model, the main concern is that funds are withdrawn at the expense of new users who want to invest in the system. Meaning that Bitcoin is rising in value because people buy it expecting it to become even more expensive.

{% hint style="info" %}
This is why short-sighted financial experts sometimes call Bitcoin a Ponzi scheme. But they are wrong - in addition to its function as a store of value, Bitcoin now also acts as a measure of value (e.g., WBTC on Ethereum) and a means of payment (Lightning Network).
{% endhint %}

But because of Bitcoin-like tokenomics, a conflict between network users and long-term holders has become apparent. Investors withdraw tokens from circulation, causing the price to rise, which raises costs for using the blockchain functionality that backs the coin. Thus, at the peak of the bull run, the commission on the use of smart contract functionality in Ethereum is prohibitive, reaching hundreds of dollars per transaction.

Imagine Netflix released its token with a limited supply, which is needed to pay for movies. Many people will want to buy it as an investment asset, causing its price to rise. Users wishing to watch movies will have to pay a lot more. This will lead to a decrease in the number of actual clients, while they are the key to the service's success and, consequently, the value of the issued token.

{% hint style="info" %}
That is why in the real world, paying for a service and investing in it are separated into two different types of assets: fiat currencies and stocks.
{% endhint %}

### Users vs Node Owners

Exchanging money for services or goods is such a simple and old concept that we don't even realize it hides a problem. It is faced mainly by people in developing countries suffering rapid currency depreciation. The local currency decline makes the population poorer since most goods in any country are imported in today's globalized world. But exporters in such countries, on the contrary, make excess profits because their income remains stable, and local costs relative to these revenues are reduced.

In the blockchain world, this problem is more pronounced as cryptocurrency users continue to live in the real world and use fiat money for living. As cryptocurrency rises, network node owners play the role of exporters in countries with weakening currencies. Their income increases while their living costs remain the same. But those who use the network for something other than investing or trading act as people getting poorer.&#x20;

{% hint style="info" %}
For example, the transaction cost has a dramatic profitability impact on online business that involves cross-border cryptocurrency payments, especially if numerous transactions are assumed.
{% endhint %}

Thus, the users' and the node owners' interests directly contradict each other. For users, commissions are costs, and it is beneficial to reduce them. For node owners, fees are income, and it is profitable to increase them. But in an ideal world, the interests of users and node owners should coincide - both groups should be interested in the growth of network popularity and its further development.

Modern blockchains solve this problem through issuance, which provides the nodes with their profitability in the first place by the very high number of newly created coins at the start of the network and the numerous initial blockchain investors. So users pay a small fee, and nodes get the bulk of the reward with minted coins. But because issuance decreases over time, at some point, one of two things will happen anyway - either the income from the emission will not be enough to motivate node owners, or the fees will drastically increase.

Even Bitcoin, having most of its coins already created and its issuance significantly reduced relative to the initial stage of blockchain development, has this problem. There is still debate in the community about what will happen when its emission drops even further or stops entirely - whether the pure fees will be sufficient to motivate node owners.

{% hint style="info" %}
At some point, the following chain of events may occur. Bitcoin issuance during the halving will drop so much that it will become unprofitable to mine in the face of such competition. The number of miners will begin to decrease, and Bitcoin's hashrate will start dropping. This will make users nervous about blockchain security, and they will begin withdrawing money from Bitcoin. The price of Bitcoin will drop, making mining even more unprofitable.
{% endhint %}

Within standard single-coin tokenomics, it is impossible to balance the user costs with the node owners' revenues because of the real-world coin price volatility. But this balance is crucial for customer availability if blockchain provides unique functionality.

## Elysium Tokenomics

It seems that it is almost impossible to make a consistent model of tokenomics on a single-coin basis - while using two coins makes it possible to resolve virtually all internal contradictions.

In general, an ideal tokenomics should facilitate the coincidence of the interests of three groups of participants:&#x20;

* Long-term holders who, having invested once, may not return to the blockchain for years.
* Regular users of the system who constantly use it for a variety of tasks.
* Validators who spend computing resources and time to keep the system running.

The coincidence of interests is not just a theoretical concept. When applied to tokenomics, it means that the growth of some functional parameter of the system must benefit all participants. Since Elysium is a truly scalable blockchain, we chose network activity, in other words, the number of transactions per unit of time, as such a parameter.&#x20;

Also, we are pretty sure that it is impossible to create a single-coin tokenomics model in which transaction growth results in gains for all participants, so Elysium tokenomics uses two coins: RAY and SKY. Their supply is managed by Elysium Grinder, which is essentially an automated central bank.

<figure><img src="../.gitbook/assets/Elysium Tokenomics.png" alt=""><figcaption><p>Elysium Tokenomics</p></figcaption></figure>

### RAY Coin

<table><thead><tr><th width="194">Parameter</th><th>Value</th></tr></thead><tbody><tr><td>Maximum Supply</td><td>Unlimited</td></tr><tr><td>Circulating Supply</td><td>Limited by formula</td></tr><tr><td>Initial Supply</td><td>1 000 000 000 RAYs during the first 1000 days</td></tr><tr><td>Inflation</td><td>5% yearly after 1000 days</td></tr><tr><td>Utility</td><td>Transaction fees in Elysium are paid in RAY</td></tr><tr><td>Issuance</td><td>Anyone can issue RAY by burning SKY in the Grinder</td></tr><tr><td>Burning</td><td>All RAYs used to pay commissions are burned</td></tr></tbody></table>

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
RAY_{issuance}=52209083\cdot\frac{e^{-0.00591626\cdot day}}{\left(1+e^{-0.00591626\cdot day}\right)^{9.6}}
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

<table><thead><tr><th width="177">Parameter</th><th>Value</th></tr></thead><tbody><tr><td>Maximum Supply</td><td>100 000 000 SKYs</td></tr><tr><td>Utility</td><td>SKY is used to issue RAY</td></tr><tr><td>Issuance</td><td>Can be minted only as validator's reward</td></tr><tr><td>Burning</td><td>A part of SKY while minting RAY is burned </td></tr></tbody></table>

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
