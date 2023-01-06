---
介绍: Elysium的一些创新
---

# 🌟 特性

Elysium是从一个单一的宏伟想法发展而来的，但现在公布还为时过早。Elysium的架构就像拼图碎片落在了合适的位置一样令人惊喜。同时，它作为下一代区块链项目解决了目前区块链面临的棘手的问题，并凭借一系列独特的功能在整个区块链领域中脱颖而出，其中任何一个功能都足以获得成功。

## 真正的去中心化

加密货币行业正日益接近中心化。在我们看来，中心化项目失去了加密货币去中心化的最初目标。权益证明（POS）对去中心化更加其具有破坏性，它导致区块链越来越趋近大资本，趋近于中心化。

在 Nassim Taleb 的一次演讲中，它举了一个例子，人们的体重可以相差5-10倍。但对于拥有的财富而言，它们可能相差10亿倍。在这样的环境中，建立一个去中心化的系统是不可能的。因为在这个系统中，一张选票的权重是绝大多数选票的数十亿倍。

Elysium的独特共识系统 - Proof of Victory - 提供了真正的，非声明式的去中心化，使得任何人都可以参与其中，如此投票的权重不取决于拥有的资本的规模。

## 无与伦比的拓展性 <a href="#4dc9" id="4dc9"></a>

Current approaches to blockchain scalability often rely on the concept of sharding, where the single data of the blockchain is split into several parts. In our opinion, this is a dead-end direction, as the very idea of storing data on multiple different tokens in one blockchain is quite absurd.

目前区块链可拓展性解决方案通常是建立分片网络，这种网络把区块链的单个数据分割成几个部分来认证。在我们看来，这是一个死胡同，因为把各式各样的Token数据存储在一条单一的区块链上的想法是非常荒谬的。

The concept of a blockchain is to store a canonical history of transactions that is important only within the context of one asset! If you have dollars and euros in your wallet, operations with dollars do not affect euros. The only time these two currencies intersect within one transaction - is when they are exchanged for each other.

Each token in Elysium will be accounted for its own independent blockchain, and each validator will be able to create blocks in many of them simultaneously. This approach allows for transactions on different tokens to be processed independently of each other. This means that high activity and load on one asset will not affect the transaction speed on others. Moreover, each new validator will increase the overall throughput of the network.

## 闪电般的速度

When people talk about blockchain speed, they often mean how quickly transactions go through, which depends primarily on finalization time. That is, how long to wait before you can be sure that the transaction will not be canceled. And there is only one condition for fast finalization - all validators need to know which of them should become the next leader and produce a new block.

In Proof of Work, there is no finalization in principle - you can never be sure that a longer chain of Bitcoin blocks will not suddenly appear out of nowhere with a completely different transaction history. Of course, the probability that aliens will arrive with overwhelming superiority in computing power or that a genius somewhere in the basement is about to finish building a quantum supercomputer is not so great. But it is not zero!

Proof of Stake consensus, on the other hand, is much better in this regard - it implies the leader's random selection in advance, depending on the size of the stakes provided by the validators. All validators immediately know who will make the next block, and the transaction speed in such networks seems almost instantaneous. But getting true randomness in fully deterministic computer systems is impossible. So a whole class of attacks on this consensus emerged, and some are impossible to defend.

In Elysium, we use the concept of occupying a future block for finalization. When creating a new block, the validator writes the future block number when he will become the leader again. It is similar to a circular queue when the leader gets back to the line after block creation. This addition to the Proof of Victory consensus allows almost instant finalization.

Thus, instant finalization, true scalability, and fast communication through a separate network layer allow Elysium to achieve unprecedented transaction processing speeds.

## 创新性的双币种经济学

Elysium Duonomics is built on the use of two different coins. The purpose of the RAY coin is to be a transaction fee payment, and the SKY coin will be needed to issue RAY. This model separates blockchain investments and transaction fees, which solves many problems at once:

* The burn mechanics of an investment SKY coin directly secures its value by the network activity - even if the number of daily transactions stays at the same level, the SKY price will continue to rise since its supply shrinks and the demand from the system remains constant.
* The growth of the SKY price will not raise the cost of transaction fees paid in RAY.
* RAY's inflation will ensure the long-term stability of commission prices relative to fiat currencies.
* Increased Elysium activity, unlike other blockchains, will reduce transaction fees.
* Burning SKY will allow its supply to be lowered gradually rather than in a leap, as in the case of Bitcoin halving.
* The separation of the commission paid in RAY and the rewards for validators accrued in SKY prevents frontrunning and makes it possible to assess the work of network nodes based on more factors besides the block production itself.

Separating tokenomics into inflationary and deflationary coins accomplishes a crucial goal. The interests of investors, users, and validators align since they all benefit from network activity growth.

## 更加易读的智能合约

Smart contracts were developed as full-fledged programs. But they are not. If you have ever touched the subject of writing smart contracts, you know that a smart contract does not run like an ordinary computer program - it does not execute entirely from start to finish. The smart contract code in current implementations is more like a library of functions that are called to handle different events.&#x20;

The logic of working with smart contracts in Elysium will be built around events handling, allowing writing such handlers in a language close to natural:

```
When contract state becomes "Fulfilled"
Then for each User
Which invested 100 Tokens
And which state is Active
Do send 120 Tokens
```

In the future, this approach will make it possible to build a visual editor for creating smart contracts without writing any code.

## 极致的安全性

The security of the Elysium wallet will be ensured not only by trivial encryption of the seed phrase when it is stored, as it is currently done by most wallets like MetaMask. In addition to the seed phrase, the user in the Elysium network will also have a seed password that will be optionally needed to confirm the use of a new wallet installation. Seed password will be required on a mandatory basis in two cases: when installing the wallet for the very first time and if you lose access to all your authorized devices.

When installing the wallet program on a new operating system or device, the blockchain at the system level will require confirmation that this installed program is allowed to dispose of funds. It can be confirmed either by the seed password or by using a wallet on an already authorized device. That way, if an attacker steals your seed phrase, he still cannot transfer your funds without knowing your seed password or having access to your device.

Elysium smart contracts will be significantly simplified compared to full-fledged Turing-complete programming languages, so the most likely ways of fraud can be automatically detected at the system level. This way, you will always be able to see the security level icon of the smart contract and, in addition, read and understand its logic on your own, even if you are not a programmer.

The ultimate effect in terms of security will be achieved by the combined work of the wallet program and the system's assessment of smart contracts. For example, if a smart contract allows the withdrawal of assets to the owner's wallet, the user will be warned when signing the transaction.

