# Glossary

# A

- **Administrator -** It is a wallet address that has certain rights to operate on the contract. It can be any address of the developer’s choice.
- **Allowance Value -** It is the amount of tokens approved by the owner of the token to be sent
- **Accuser** - The accuser is a daemon that monitors all blocks received. It looks for two indications of invalid blocks:
    - When a baker has signed two blocks at the same block height (blocks at the same level);
    - When an endorser injects more than one endorsement operation for the same baking slot.

# B

- **Better** **call** **dev -** Better call dev is a contract explorer for Tezos. It plays a crucial role in smart contract development, testing, and interaction in Tezos.
- **Beacon -** Beacon is a middleware that facilitates the connection between dApps and wallets.
- **Big** **map -** A key-value pair database of a smart contract. The values are fetched on-demand during smart contract invocation, making it scalable for holding a large number of entries.
- **Baker -** In Tezos, block creators are referred to as bakers. As the name suggests, the baker is responsible for baking (producing) new blocks.

# C

- **Contract Storage** - It can be interpreted as a database in web 2.0. The data is stored on a contract, and it defines the state of the contract. Only the contract can edit the storage.
- **Contract metadata -** Contract metadata stores basic information of a contract. E.g name, description, standards, etc.

# D

- **DeFi -** DeFi stands for Decentralized Finance. It refers to the shift from traditional, centralized financial systems to peer-to-peer finance enabled by decentralized applications built on Tezos.
- **DApp** -  It is a decentralized app. It is like normal apps and offers similar functions, but the key difference is that it runs on a peer-to-peer network, such as a blockchain.

# E

- **Entrypoint** - It is like a function in web 2.0 that can be called to interact with the contract.
- **Escrow -** An escrow is a contract that facilitates the trustless exchange of assets between two parties
- **Endorser -** Like the baker, the endorser is connected to an implicit account and computes endorsing rights on a per-account basis based on a baker’s total stake. On receipt of new blocks it verifies the validity of the block. If the block is valid it will broadcast an endorsement operation.

# F

- **FA(Fungible Assets) -** A fungible asset is a divisible and non-unique token that can be traded or exchanged, one for another.

# G

- **Gas fee** - It is the cost of computation to execute an operation on-chain.

# I

- **Indexer -** You can use it to see most blockchain data easily, including but not limited to anyone's transactions, token balances, baking rewards, etc.
- **IPFS -** The InterPlanetary File System is a protocol and peer-to-peer network for storing and sharing data in a distributed file system.
- **In** **memory** **signer -** It is ****a ****package useful for development and testing. It's an easy way to get started with Tezos when you don't need to interact with a user's wallet.

# L

- **Ledger -** A ledger is a database of balances of tokens held by different wallet addresses.
- **Ligo -** It is a language for smart contract development on tezos.

# M

- **Mainnet -** It is the main running network on the Tezos protocol. The tokens on mainnet have real value.
- **Michelson** - It is a domain-specific low-level programming language for smart contract development on Tezos.
- **Metadata -** Some information about any data.
- **Mutez -** It is the smallest unit of tezos. `1 tez = 1000000 mutez`
- **Multisig -** A multi-signed account, or multisig for short, is a way to share the ownership of an address (and of the associated balance) between several participants.
- **Minting -**  The process of creating a token.

# N

- **Non-fungible Token -** NFTs (non-fungible token) are unique virtual assets that are basically some data stored on the blockchain which has some value. It can be a piece of art, audio, video, or even a tweet.
- **Node -**

# O

- **Off-chain -** Anything that occurs or exists outside the blockchain.

# P

- **Public key** - It is the counterpart of the private key, that can be used to verify if a transaction is signed by its corresponding private key or not.
- **Public key hash** - It is a shorter string (hash of public key) for uniquely identifying wallets. It is more popularly known as wallet address or implicit account address. It is a 36 character long string starting with tz1, tz2 or tz3.
- **Private key** - It is a long string that is algorithmically derived from a seed phrase. As the name suggests, it is meant to be kept secure and private. It is used to sign transactions.
- **PyTezos -** PyTezos is a Python library for interacting with Tezos blockchain and testing smart contracts.

# R

- **RPC** - It stands for Remote Procedure Call. An RPC interface is an API that allows developers to communicate to a server in order to remotely execute code. Tezos nodes offer an RPC interface for dApps to interact with the Tezos network.

# S

- **Smart Contract -** It is a computer program that executes and controls relevant events and actions. The code and the agreements contained therein exist across a distributed, decentralized blockchain network.
- **SmartPy** - It is an intuitive and powerful smart contract development platform for Tezos. SmartPy Reference - [https://www.notion.so/SmartPy-Cheatsheet-6cb48b78d1ae4a0ca0c62d86f5462e95](https://www.notion.so/SmartPy-Cheatsheet-c9d12639a93a436e9d76cd0b664e6079)
- **Storage fee** - It is the cost of storage on the blockchain. It is directly proportional to the bytes added to the contract storage by an operation.
- **Smart Contract** **Explorer -** A tool used to view smart contract storage on blockchain and interact with them.
- **SmartPy Explorer -** SmartPy explorer is a tool used to interact with the contract and view its storage.
- **Seed Phrase** - It is a long phrase of 12 to 24 random words used to generate a private key. It is meant to be kept private.

# T

- **Tezos** - It is a public, open-source blockchain protocol relying on low power consumption and energy-efficient consensus known as Liquid Proof of Stake(LPOS).
- **Tez -** The native currency of Tezos blockchain.
- **TZIP** - It stands for Tezos Improvement Proposal. TZIPs are documents that offer ways to improve Tezos via new features, tools, or standards.
- **Temple wallet -** Temple Wallet is an open-source and easy-to-use browser extension wallet for interacting with the Tezos Ecosystem.
- **Testnet** - Testing network on tezos blockchain. Tokens on testnet don’t have a monetary value.
- **Tokens -** Tokens are digital assets that are stored on the blockchain. They are defined by a set of rules encoded in a smart contract.
- **Taquito -** A TypeScript/Javascript library suite for developing dApps.
- **Token metadata -** Token metadata is intended for off-chain, user-facing contexts (e.g. wallets, explorers, marketplaces). It includes information such as name, symbol, description, thumbnail, image or linked multimedia, etc.
- **tzkt -** [TzKT.io](https://tzkt.io/) is a blockchain indexer and explorer for Tezos. You can use it to see most blockchain data easily, including but not limited to anyone's transactions, token balances, baking rewards, etc.

# V

- **Validator -** A validator is an individual or organization that proposes and verifies blocks in a **Proof of Stake** network. Validators may stake their own coins, accept **delegations** from other holders, or both.

# W

- **Wallets** - Digital wallets that allow users to store and manage their crypto assets and interact with dApps.
- **Wallet Address - I**t is a shorter string (hash of the public key) for uniquely identifying wallets. It is more popularly known as a wallet address or implicit account address. It is a 36 character long string starting with tz1, tz2 or tz3.

# X

- **XTZ -** It is the currency symbol of *tez*.