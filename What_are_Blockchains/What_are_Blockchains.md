# What are Blockchains

Before we start digging into Tezos itself, let's review the basics of blockchain and cryptocurrencies. This module will present a brief history of the blockchain, its main components, consensus mechanisms, and the use cases of blockchain.

## Introduction

A blockchain is a decentralized ledger of all transactions across a peer-to-peer network. Using this technology, participants can confirm transactions without a need for a central clearing authority. 
The blockchain is an **immutable** - (unchangeable, meaning a transaction or file recorded cannot be changed) **distributed digital ledger** (digital record of transactions or data stored in multiple places on a computer network) with many use cases beyond cryptocurrencies. 

[History of Blockchain Technology: A Detailed Guide](https://101blockchains.com/history-of-blockchain-timeline/)

## Structure of Blockchain

Blockchains are decentralized records. Instead of being stored in one central location, the blockchain is stored on the computers of every user of that given blockchain. Blockchains are made up of blocks that are linked to each other by a hash which is unique for every block.

The first block in a blockchain is called the **genesis block.** 

A **block** contains:

- A batch of valid **transactions**
- **Hash of the block *-** It is* a hexadecimal number and is always unique. It connects all the blocks in a blockchain. If the data changes in a block, the hash also changes.
- **Hash of the previous block *-*** Every block stores the hash of its previous block.

![assets/Group_13_(1).png](assets/Group_13_(1).png)

<aside>
💡 Learn more about the basic working of blockchain [here](https://www.youtube.com/watch?v=SSo_EIwHSd4&t=37s)

</aside>

## How do Blockchains Work?

The chaining of blocks by their hashes, as described above, makes blockchain immutable. As the block is derived from the information contained in the previous block in the blockchain, tampering with a block will make all the blocks after it invalid. But, nowadays computers are fast enough to recalculate hashes of all the blocks and to make blockchain valid again. Therefore hashing itself is not enough to prevent tampering.

In order to make blockchain more secure, it is **distributed over a network**, which means valid blocks have to be replicated on all network nodes. Everyone connected to the network has a full record and copy of the blockchain. When a new block is created, it is sent to everyone to verify if it is tampered with. All nodes create a **consensus** and **validate** a block. If the block validates then it is added to all the nodes.

This means that, in order to falsify any record on the blockchain, a nefarious actor would have to **change every block** on every instance of the blockchain. As a result, **blockchains** are considered to be virtually **unfalsifiable** and are thought of as **immutable** records of **transactions**. 

Today, most blockchains are public. This includes prominent cryptocurrencies such as **Bitcoin** and **Ethereum**. Anyone can view records of transactions conducted on a given blockchain, using a tool called **block explorer**. 

Theoretically, however, blockchains afford a high level of **anonymity** to users. While **public blockchains** are the norm, **private versions** are also being explored as a solution for many business and government use cases.

## Consensus Mechanism

A consensus mechanism is an algorithm that allows users to reach common agreements on the states of blockchain in a distributed network. Different blockchains use different consensus mechanisms.

<aside>
💡 Many blockchains, including Bitcoin and Ethereum, use **Proof-of-Work** as their consensus mechanism.

</aside>

### Proof of work

Being the first cryptocurrency to be created, bitcoin’s Proof-of-Work protocol was the first fully functional blockchain consensus mechanism ever created. Proof-of-Work requires its users to validate blocks of transactions in order to earn rewards. This process is called “mining”.

Users/miners solve a mathematical puzzle by calculating the hash of a block repeatedly until it achieves the validation rule. A widely used validation rule is that hash must start with *0000*.

The first miner to solve the puzzle gets to create the next block and if the block is validated then it is added to the blockchain and the miner gets some rewards.

### Proof of Stake

Many blockchains, including Tezos use proof-of-stake consensus mechanisms — to maximize speed and efficiency while lowering cost.

In a Proof-of-Stake system, "stakers" replace the role of miners. These "stakers" add the latest batch of transactions to the blockchain and earn some crypto in exchange. Proof-of-Stake blockchains employ a network of “validators” who contribute — or “stake” — their own crypto in exchange for a chance to validate new transactions, update the blockchain, and earn a reward. Details of staking vary from different blockchains. 

- The network selects the winner based on the length and amount of crypto/coins each validator has in the pool - rewarding the most invested participants.
- Once the winner has validated the latest block of transactions, other validators in the network will attest that the block is accurate. The blockchain gets updated when a threshold number of attestations have been made.
- All participating validators receive a reward in the native cryptocurrency, which is generally distributed by the network in proportion to each validator’s stake.

Becoming a validator is a major responsibility and requires a fairly high level of technical knowledge.

Proof-of-Stake comes with a number of improvements to the proof-of-Work system:

- better energy efficiency – you don't need to use lots of energy mining blocks.
- lower barriers to entry – you don't need high power computers to stand a chance of creating new blocks.
- stronger immunity to centralization – Proof-of-Stake should lead to more nodes in the network.

## Some use cases of Blockchain

Blockchains are not just confined to cryptocurrency. Since it ensures transparency and security, it is impacting many sectors of our economy. Its use cases are endless, out of which some are listed below:

- **Capital Markets** - Blockchain technology allows for easier, faster and cheaper access to capital. For example, it enables peer-to-peer trading, quicker and transparent settlement of payments additionally it also allows for reduced costs and counterparty risks, and streamlined auditing and compliance.
- **[DeFi](https://dappradar.com/rankings/protocol/tezos/category/defi)** - Stands for Decentralized Finance. It refers to the shift from traditional, centralized financial systems to peer-to-peer finance enabled by decentralized applications built on Tezos. This new economic system is setting a financial standard for access, opportunity and trust in which anyone can build and participate in it.
- **[NFT](https://dappradar.com/rankings/protocol/tezos/category/marketplaces)** - A non-fungible token is some data stored on a blockchain, that certifies a digital asset to be unique and therefore not interchangeable. NFTs can be used to represent data such as digital art, video, audio, and other types of files.
- **Digital voting** -Blockchain to cast and store votes instead of in-person paper voting. This will make the process significantly more transparent and tamper-proof as the the record is immutable.

