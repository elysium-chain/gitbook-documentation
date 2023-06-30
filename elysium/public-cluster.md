---
description: New architecture for decentralized systems.
---

# 💠 Public Cluster

## **The rise and fall of peer-to-peer architecture.**

The concept of decentralization is quite broad and includes many aspects from various domains: politics, sociology, game theory, engineering, programming, and economics. So when we describe a computer system as decentralized, we must accent particular aspects we discuss. And usually, decentralization refers to a peer-to-peer architecture that is a network of equal and interchangeable nodes.

{% hint style="info" %}
The pure peer-to-peer approach assumes that nodes that form a network provide a service to each other. A computer program allows a user to get resources from different nodes, and at the same time, it acts as a server that processes requests from other participants. A good analogy is a barbershop society, where members can ask others for a free haircut.
{% endhint %}

However, only some peer-to-peer networks are genuinely decentralized systems since there are often centralized services running on top of a peer-to-peer network to help nodes communicate with each other. Therefore, distributed systems such as BitTorrent, SETI@home, or Skype are, in fact, something in between.

But every existing decentralized system is based on a peer-to-peer architecture since this is the only available alternative. The problem is that all such systems inherit the intrinsic weaknesses of peer-to-peer.

#### The birth of the peer-to-peer concept

The idea of a network made of equal nodes appeared due to the rapid growth in the popularity of personal computers, which gave unlimited freedom to individual users. It seemed then that ordinary users could collaborate without a central authority, such as large corporations or states, by uniting and sharing resources with each other.

But the actual implementation of the peer-to-peer concept (1984) became possible 20 years after its inception. Only in the early 2000s, most users switched to multitasking operating systems on which peer-to-peer node software did not block the rest of the functionality, and a dedicated Internet connection actively began to displace dial-up.

#### Failed attempts to create decentralized peer-to-peer file storage

The main task, which the first peer-to-peer systems tried to solve, was the implementation of distributed file storage based on home computers. And in practice, the fundamental limitation of such systems immediately became apparent.&#x20;

It turned out that in a pure peer-to-peer network, achieving an effective search over the files stored on the nodes is impossible. It is because only the files that can be downloaded right away should be searched. In other words, the request should be made only for those nodes that are working at the time of the search. But within a decentralized peer-to-peer public network, getting an up-to-date list of working nodes is unrealistic.

Therefore, the only way to search is to transfer the request from one node to another. But since nodes constantly connect and disconnect from the network, search requests will never be completed as the list of available files in the system is continuously changing. And limiting the lifetime of the request lowers its probability of reaching the node where the desired file is stored.

{% hint style="info" %}
Searching for a file in an unstructured peer-to-peer network can be compared to exiting a constantly changing maze. The only way to find a way out (if there is one) is to get lucky during a random walk. It is one of the facets of a routing problem in a decentralized network.
{% endhint %}

#### Blockchain - a new twist in the evolution of peer-to-peer systems

Apart from building file storage, there have also been attempts to create peer-to-peer systems for distributed computing. But all such projects (e.g., SETI@home) had some degree of centralization in their architecture.

Bitcoin was the first genuinely decentralized peer-to-peer system that used distributed computing to protect the canonical transaction history. And at first, this approach worked well - the bottlenecks caused by the peer-to-peer architecture appeared later.

The first problem encountered was [IP address exhaustion](https://en.wikipedia.org/wiki/IPv4\_address\_exhaustion). The protocol IPv4 (1981), still taking up most of the Internet traffic, assumes just over 4.2 billion addresses - less than all devices connected to the Internet nowadays.

{% hint style="info" %}
Most technologies result from coincidence and chance - [according to Vint Cerf](https://www.youtube.com/watch?v=mZo69JQoLb8\&t=816s), the Internet is an experiment escaped from a laboratory.
{% endhint %}

Ordinary users do not notice the lack of IP addresses. But it is a severe limitation for peer-to-peer expansion since nodes must interconnect to form a network. Due to the lack of IP addresses, most home computers are connected to the Internet through [NAT](https://en.wikipedia.org/wiki/Network\_address\_translation), which does not allow them to [interconnect directly](https://pdos.csail.mit.edu/papers/p2pnat.pdf) without the help of a third-party server with a public IP address.

The second problem is the constant growth of the number of transactions and, consequently, the size of the blockchain. Today, the Bitcoin blockchain exceeds 430GB, so it would take days to download all the blocks and verify the chain for the initial launch of the node.

The massive blockchain size creates a high entry barrier for newcomers since the peer-to-peer approach implies that any interaction with the system, even making an own transaction, requires a personal node.

And the third problem is the exponential growth of the Bitcoin price, which contributes to intense competition for participation in its issuance. The competition among miners became so high that the probability of creating a new block using an ordinary computer and, hence, receiving a reward for it dropped to almost zero.

{% hint style="info" %}
Big farms built from specially designed devices (ASICs) create most of the new blocks nowadays. The largest of such farms belong to the manufacturers of ASICs themselves. So the big players have taken over Bitcoin issuance, taking it far from the original peer-to-peer idea of equality.
{% endhint %}

Thus, using the functionality embedded in Bitcoin nodes on home computers has become virtually impossible.

Nodes were divided into different types depending on their tasks to solve these problems. A _miner_ is a particular client for farms designed for block generation. A _light node_ acts as a wallet for ordinary users. A _full node_ is the analog of the server and plays the role of a verifier, a database storage, and network gateway.

Dividing nodes into different types solved most of the problems accumulated in Bitcoin. But it also broke the original logic - full nodes contribute to the network the most, although they do not receive a reward.

#### The decline of peer-to-peer

Splitting nodes into different types is not exclusive to Bitcoin - the developers of almost all modern blockchains build multiple types of nodes into their architecture, which takes blockchain technology further and further away from the equality and interchangeability of nodes.

So, we can now confidently declare the failure of the pure peer-to-peer approach. Moreover, many centralized solutions seem so natural that we don't even notice them. For example, when you send transactions to the blockchain via MetaMask, analyze transactions in a blockchain explorer, or upload a file to IPFS - you are using the client-server approach - the antagonist of peer-to-peer.

And this is not a bad thing because what really matters is not the technical principles of interaction between computers but the idea of independence from regulators setting their own rules, which the peer-to-peer concept symbolizes.

The bad thing is that on the bright side of fairness, there is no alternative to the ancient peer-to-peer architecture, which has not defeated its inherent limitations in 40 years of development.

It's time to invent something new, especially since blockchain technology has opened up new horizons.

## Public cluster

Although the concept of decentralized computer systems appeared as a synonym for peer-to-peer architecture, they are not the same. While peer-to-peer is the principle on which the system is built, decentralization is a set of properties it possesses. We consider the absence of an owner who controls the system's critical infrastructure as the most important of these properties. In other words, a truly decentralized system has no master.

Cryptocurrencies' phenomenal success is primarily because the lack of an owner removes many political risks from the system. After all, when there is no managing center, no one can change the rules to their benefit, users do not need to be authorized to participate, and third parties, such as competitors or government agencies, cannot influence the system through pressure on a particular person or company.

But when there is no owner, there is also no single source of truth to which all participants can refer.&#x20;

{% hint style="info" %}
The owner, for example, can determine which server provides the current time, keeps a list of all working nodes, or stores the file paths. But such a server becomes known to everyone, and if a third party blocks it, the system will stop working. And this has happened more than once.
{% endhint %}

Theoretically, a majority consent of the nodes about the system's state could serve as the source of truth. The participants' individual interests are contradictory, and, as a result, the optimum to which the system will aim is the balance of the interests of the majority of its participants.

<figure><img src="../.gitbook/assets/One node – one vote.webp" alt=""><figcaption></figcaption></figure>

But in practice, an attacker can get many of the nodes in a system under his control simply by creating them, thus obtaining the majority and biasing the consent in his favor. This type of threat of privatization of an ownerless system by one of its participants has been named Sybil attacks.

<figure><img src="../.gitbook/assets/Sybil attack.webp" alt=""><figcaption></figcaption></figure>

The primary method of defending against this kind of attack is competition among participants for limited resources. And this approach was first used in the Bitcoin network, where voting for the canonical chain of blocks is not about the number of nodes under a participant's control but about computing resources, which require not only the initial investment but also a constant expenditure of electricity.

Thus, the Proof of Work consensus is based mainly on a protection mechanism against Sybil attacks. And so is Proof of Stake, which uses tokens stored in the blockchain instead of calculations.

<figure><img src="../.gitbook/assets/Preventing Sybil attacks.webp" alt=""><figcaption></figcaption></figure>

In fact, starting with Bitcoin, all subsequent truly decentralized blockchains use consensus with built-in protection against Sybil attacks, as only this approach allows using a peer-to-peer architecture.

But the protection against Sybil attacks can be separated from the consensus by taking the security dome outside the system. An attacker can only hack the formula "one node - one vote" if there is no barrier for new nodes. If, however, participants must compete with each other to join the system, the threat of Sybil attacks is eliminated long before the consensus process itself.

<figure><img src="../.gitbook/assets/Preventing Sybil attacks before....webp" alt=""><figcaption></figcaption></figure>

Moreover, protecting the network from fake nodes allows us to move away from the peer-to-peer architecture while maintaining the ownerless concept. After all, the motivation of nodes through the issuance of blockchain assets significantly impacts the network's size and configuration.

And if, until now, this property has been applied only as a motivation to expand a flat peer-to-peer network in _**breadth**_, we propose to use the limited blockchain resources to form a hierarchy of nodes in _**depth**_.

In other words, the limited virtual assets that became available with the advent of the blockchain concept can be used not only to create cryptocurrencies but also as a means to build a hierarchy.

This approach adds a new dimension of complexity to the architecture of a decentralized system, allowing it to dramatically increase its efficiency through a division of labor not achievable with a pure peer-to-peer architecture.

We call this type of architecture a Public Cluster.

> **A Public Cluster is an architecture of an ownerless system formed by vertically linked hierarchical layers that require limited blockchain resources to participate in. Every layer, which consists of equal and interchangeable nodes, can be a distinct peer-to-peer network.**

<figure><img src="../.gitbook/assets/Public cluster is formed by....webp" alt=""><figcaption></figcaption></figure>

While in classic Proof of Work, real computing power protects the virtual blockchain from tampering, in a public cluster architecture, virtual blockchain resources shield the physical network from the fake nodes.

{% hint style="info" %}
Imagining a chain of blocks as a rope, when woven with Proof of Work consensus, the nodes weave a gold thread into it. And in a public cluster, virtual gold is demanded from the nodes to be part of the device, producing a rope with unique coloring.
{% endhint %}

The public cluster architecture has a whole set of unique advantages:

* Ownerless design. There are no political risks, meaning that no participant can change the system's rules in his interest, so there is no single point of failure in the form of a person or company that a third party can push.
* Decentralized source of truth. The information on higher hierarchical layers that nodes agree on can be a single source of truth for lower layers, preventing an attacker from misleading other participants. In other words, a single owner is replaced by a decentralized hierarchical layer consisting of multiple nodes. It opens up a way to solve BFT problems in entirely new areas. For example, for the first time, it is possible to make unicast forwarding of messages between nodes in a decentralized system by building a structured topology on one of the hierarchical layers.
* Permissionless system. Any (but not every) user can run his node at one of the hierarchy levels without any approvals from the authorizing center, which does not exist. At the same time, the lowest level may not require resources to participate, thus allowing anyone to support the system.
* Consensus simplification. When there is no need to build Sybil attack protection into the consensus mechanism, multiple independent parameters can be used to select the next block. In addition, block agreement by a limited number of nodes at the top - the safest - hierarchical level ensures decentralized, secure, and fast consensus.
* High efficiency. The hierarchy of the public cluster allows sequential information processing, i.e., according to the conveyor principle. For example, if preprocessing on one of the hierarchical layers generates blocks from transactions as a blockchain-state patch and zk-SNARK, the other layer will update the data almost instantaneously. Theoretically, it allows a decentralized system to surpass the limits of information processing by a single server, which until now has been an unsolvable task.

But there is always a price to pay for improvements.

First, starting a public cluster is a challenge because it must already consist of many independent participants when it first launches. Therefore, a separate system of pre-selection of participants is needed to start a cluster in a decentralized state, preventing the centralization of nodes in a single hand from the very beginning.

Second, when the public cluster is already running, there should be a system for allocating the resources needed to participate in the hierarchical layers. Competition for these resources is the key to long-term decentralization, so the principles of their distribution play a crucial role in the system's overall reliability. After all, centralizing these resources allows a malicious actor to establish control over most layer nodes and potentially disrupt the entire cluster.

Third, the system's stability to malicious behavior of the participants is a rather complex logical problem, solved in each case individually. Every rule should have an algorithm protecting it from evil actors. Therefore a straightforward principle applies: the more rules exist in the system, the more difficult it is to ensure their guaranteed implementation. And some types of such rules cannot be protected at all.

Fourth, limited access to hierarchical layers means dynamic node rotation, which requires a relatively quick and easy inclusion in blockchain support without downloading hundreds of gigabytes.

### Elysium public cluster

The Elysium public cluster consists of three hierarchical layers connected vertically: an assertion layer, an address layer, and an assembly layer.

The assertion and address layers are formed as peer-to-peer networks. While the assertion layer has an unstructured topology, the address layer has a structured topology.

The entire cluster acts as a server, providing service to clients connecting to the address layer.

<figure><img src="../.gitbook/assets/Elysium Public Cluster.webp" alt=""><figcaption></figcaption></figure>

#### Assertion layer

The assertion layer is an unstructured peer-to-peer network formed by Keepers. Meaning, Keepers do not create any structured topology and interconnect randomly.

The Proof of Victory consensus works on the assertion layer, as it is at the very top of the hierarchy and, as such, is the most secure and decentralized layer. The logic of Proof of Victory is designed to guarantee that the consensus will be reached as long as 51% of Keepers are correctly working.

The only thing an evil Keeper can do to harm the system is to not work. More precisely, any malicious actions will produce the same results as if the Keeper did nothing.

#### Address layer

Most of the tasks on the Elysium network are performed on the address layer by Routers. They maintain the blockchain, verify transactions and blocks, function as network gateways, and act as the core mail service for sending tokens between users.

Forming a structured address ring is one of the most important architectural features of the address layer. Routers, acting as gateways, connect Workers and Wallets to the address ring, effectively creating a consistent network for clients with a single address space based on the blockchain addresses.

A single address space effectively solves many problems decentralized systems face, from user-friendly client-server interaction to the addressable forwarding of crypto assets and information.

{% hint style="info" %}
In other words, the user's wallet program will not connect to proprietary servers, as with virtually all current solutions, but to one of the Routers. In addition, sending requests to a specific wallet and receiving a response from it will be possible in the Elysium network.
{% endhint %}

In addition to their primary tasks at the address level, Routers also act as a liaison to tie the entire cluster together. This is achieved through vertical layer integration, as Workers and Wallets connect to Routers, which in turn must be connected to Keepers.

Every new block passes from Worker through Router to Keeper, and each of these node types is rewarded. It promotes the match of interests of node owners on different hierarchies, which leads to motivation for vertical integration of the layers.

#### Assembly layer

In contrast to Routers and Keepers, which must run on a server with a public IP address, a Worker is a regular program for a home computer (Windows, MacOS, or Linux). Its logic is simple - the program packs unprocessed user transactions into a block and gets a reward if it is selected as the next block in the blockchain.

It is worth noting that the Worker's task is only to create a new block, not to reach a consensus. In other words, block creation does not require unnecessary computation, as in Proof of Work.

Separating the new block creation (which requires checking the correctness of the previous chain) into a distinct role brings much greater decentralization of the nodes that support and check the system's work. At the same time, this approach reduces as much as possible the technical entry barrier for node owners - only a program running on a home computer or laptop that does not consume many resources is required.

{% hint style="info" %}
A relatively close analogy for describing the architecture of Elysium can be a bank. Thus, the Keepers correspond to the bank's board of directors, which decides critical issues and is the only source of truth. Routers can be compared to a network of branches, which regular customers can visit to make transfers, as well as Workers, who perform specific tasks for a reward.
{% endhint %}

#### The launch and the size of the Elysium public cluster

To be able to connect to each of Elysium's hierarchical layers, one of the unique non-tradable on-chain assets will be required: Bronze (Workers), Silver (Routers), and Gold (Keepers).

The blockchain system of distributing these assets to all participants involved in Elysium will be launched sometime after the system's launch. Initially, the public cluster will be formed by participants who have successfully passed the [Pioneer Program](../join/pioneer-program.md). Pioneers will be able to launch their nodes on one of the hierarchical layers, depending on the results they achieve in the Program.

{% hint style="info" %}
There will be selected 70 participants as Keepers, 500 as Routers, and 1000 as Workers (maybe more). External users will not be able to join any layer before launching a Bronze, Silver, and Gold distribution. From the initial launch of the system until the start of the distribution system, the public cluster will operate in a test mode with real SKY rewards for pioneers.
{% endhint %}

The details of how the Bronze, Silver, and Gold distribution system will work once it is launched will be covered in a separate section, as this topic is broad. For now, it is essential to note that Silver will, on average, be ten times more scarce than Bronze and ten times more affordable than Gold.

Since the total reward per block is limited, increasing the number of nodes will lead to a proportional decrease in participants' profits. In addition, some critical aspects of the system, such as consensus, will run slower with more nodes. That is why the number of nodes of different types should aim for an optimal value to better balance the system's reliability and decentralization with performance and profitability.

{% hint style="info" %}
The final sizes of the different groups of nodes will be obtained from the network testing data, but for now, we can be guided by the following rough numbers:

* Keepers: 101
* Routers: 1001
* Workers: 10001
{% endhint %}

The motivation for increasing the number of nodes will be a reward in SKY coins. The SKY for each block is distributed between a Worker, a Router, and a Keeper evenly. Thus, simply because there are ten times fewer Keepers than Routers, their income will be, on average, the same ten times higher. In other words, increased profitability on higher hierarchy levels will be due to reduced competition.

Limiting the growth of the number of nodes when reaching the optimal value will be achieved by constantly charging resources from all nodes of this type. And the higher the optimal number is exceeded, the greater the corresponding resource will be charged off. Resources will not be charged when the number of nodes is less than optimal.

In other words, if there are 1000 Routers, they will not be charged Silver. If there are 1001, they will be charged 1x Silver. And when they reach the total of 2002, 2x Silver will be charged.

Since the amount of Silver held by each Router will be different, at a certain point, some of them will run out of Silver, and those nodes will no longer be able to perform the role of a Router. Therefore, the more Routers there are, the faster their quantity will aim to optimal.

{% hint style="info" %}
Whereas Bitcoin can be obtained as a reward for expending computational resources, SKY can be obtained by spending on-chain non-tradable resources - Bronze, Silver, and Gold, backed by the engagement of participants.
{% endhint %}

## Summary

The Elysium public cluster's hierarchy and logic allow it to achieve several contradictory goals.

First, an opportunity arises to bring back the spirit of the early days of the crypto-industry, when to enter the world of cryptocurrencies, you didn't even have to buy them - you just had to run a program on your home computer and after a while the cryptocurrency appeared in your wallet all by itself. In Elysium, we will bring that utopia back.

Second, since there are relatively few Keepers participating in the consensus, the time of agreeing on a new block will be minimal because the most significant influence on the speed of the agreement is the time of information distribution over the network, which is higher as more nodes form the network. The consensus is achieved on the most protected hierarchical layer, which excludes many types of attacks (including Sybil and DDoS attacks). However, a new attack vector opens up, which we will discuss separately in the consensus section.

Third, addressable messaging allows many problems (e.g., interaction with the outside world) to be approached from a new and unexpected perspective.

Fourth, the hierarchical layers make it possible to build information processing sequentially, achieving record-breaking throughput.
