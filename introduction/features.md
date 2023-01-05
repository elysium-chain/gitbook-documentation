---
description: Elysium is made of innovations
---

# 🌟 Features

The logic of Elysium grew from a single Big Idea, which is still early to unveil. It is amazing how the architecture of the blockchain self-assembled around it, as if the puzzle pieces fell into place. The result is a next-generation blockchain project that solves almost all existing problems and stands out among other networks with a set of unique features, any one of which would be sufficient for success on its own.

## Real Decentralization

The cryptocurrency industry is increasingly shifting towards centralization. But centralized projects, in our understanding, lose the very idea that made cryptocurrencies so attractive in the first place. Proof of Stake is particularly destructive to decentralization, as it declares decentralization through the capital.

In one of his talks, Nassim Taleb gave an example that people can vary from each other in weight by 5, well by 10 times at max. But in the size of their fortunes, they can differ a billion times. How can a decentralized system be created where one vote weighs billions of times more than the overwhelming majority of others?

The unique consensus of Elysium - Proof of Victory - provides real, rather than declarative decentralization, as anyone can participate in it, and the weight of the vote does not depend on the size of the owned capital.

## True Scalability <a href="#4dc9" id="4dc9"></a>

Current approaches to blockchain scalability often rely on the concept of sharding, where the single data of the blockchain is split into several parts. In our opinion, this is a dead-end direction, as the very idea of storing data on multiple different tokens in one blockchain is quite absurd.

The concept of a blockchain is to store a canonical history of transactions that is important only within the context of one asset! If you have dollars and euros in your wallet, operations with dollars do not affect euros. The only time these two currencies intersect within one transaction - is when they are exchanged for each other.

Each token in Elysium will be accounted for its own independent blockchain, and each validator will be able to create blocks in many of them simultaneously. This approach allows for transactions on different tokens to be processed independently of each other. This means that high activity and load on one asset will not affect the transaction speed on others. Moreover, each new validator will increase the overall throughput of the network.

## Lightning Speed

When people talk about blockchain speed, they often mean how quickly transactions go through, which depends primarily on finalization time. That is, how long to wait before you can be sure that the transaction will not be canceled. And there is only one condition for fast finalization - all validators need to know which of them should become the next leader and produce a new block.

In Proof of Work, there is no finalization in principle - you can never be sure that a longer chain of Bitcoin blocks will not suddenly appear out of nowhere with a completely different transaction history. Of course, the probability that aliens will arrive with overwhelming superiority in computing power or that a genius somewhere in the basement is about to finish building a quantum supercomputer is not so great. But it is not zero!

Proof of Stake consensus, on the other hand, is much better in this regard - it implies the leader's random selection in advance, depending on the size of the stakes provided by the validators. All validators immediately know who will make the next block, and the transaction speed in such networks seems almost instantaneous. But getting true randomness in fully deterministic computer systems is impossible. So a whole class of attacks on this consensus emerged, and some are impossible to defend.

In Elysium, we use the concept of occupying a future block for finalization. When creating a new block, the validator writes the future block number when he will become the leader again. It is similar to a circular queue when the leader gets back to the line after block creation. This addition to the Proof of Victory consensus allows almost instant finalization.

Thus, instant finalization, true scalability, and fast communication through a separate network layer allow Elysium to achieve unprecedented transaction processing speeds.

## Innovative Duonomics

Elysium Duonomics is built on the use of two different coins. The purpose of the RAY coin is to be a transaction fee payment, and the SKY coin will be needed to issue RAY. This model separates blockchain investments and transaction fees, which solves many problems at once:

* The burn mechanics of an investment SKY coin directly secures its value by the network activity - even if the number of daily transactions stays at the same level, the SKY price will continue to rise since its supply shrinks and the demand from the system remains constant.
* The growth of the SKY price will not raise the cost of transaction fees paid in RAY.
* RAY's inflation will ensure the long-term stability of commission prices relative to fiat currencies.
* Increased Elysium activity, unlike other blockchains, will reduce transaction fees.
* Burning SKY will allow its supply to be lowered gradually rather than in a leap, as in the case of Bitcoin halving.
* The separation of the commission paid in RAY and the rewards for validators accrued in SKY prevents frontrunning and makes it possible to assess the work of network nodes based on more factors besides the block production itself.

Separating tokenomics into inflationary and deflationary coins accomplishes a crucial goal. The interests of investors, users, and validators align since they all benefit from network activity growth.

## Natural language smart contracts

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

## Uncompromising Safety

The security of the Elysium wallet will be ensured not only by trivial encryption of the seed phrase when it is stored, as it is currently done by most wallets like MetaMask. In addition to the seed phrase, the user in the Elysium network will also have a seed password that will be optionally needed to confirm the use of a new wallet installation. Seed password will be required on a mandatory basis in two cases: when installing the wallet for the very first time and if you lose access to all your authorized devices.

When installing the wallet program on a new operating system or device, the blockchain at the system level will require confirmation that this installed program is allowed to dispose of funds. It can be confirmed either by the seed password or by using a wallet on an already authorized device. That way, if an attacker steals your seed phrase, he still cannot transfer your funds without knowing your seed password or having access to your device.

Elysium smart contracts will be significantly simplified compared to full-fledged Turing-complete programming languages, so the most likely ways of fraud can be automatically detected at the system level. This way, you will always be able to see the security level icon of the smart contract and, in addition, read and understand its logic on your own, even if you are not a programmer.

The ultimate effect in terms of security will be achieved by the combined work of the wallet program and the system's assessment of smart contracts. For example, if a smart contract allows the withdrawal of assets to the owner's wallet, the user will be warned when signing the transaction.

