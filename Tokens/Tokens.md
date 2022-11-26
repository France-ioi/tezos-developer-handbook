# Tokens

Tokens are digital assets that are stored on the blockchain. They are defined by a set of rules encoded in a smart contract. Each token belongs to a blockchain address. They can be bought, sold, or exchanged between users.

Tokens have a very broad set of use cases in the whole blockchain industry. Some of which are listed below:

- **Cryptocurrency** - A cryptocurrency is a form of token that can have monetary value and can be traded for other assets.
- **NFTs** - NFTs (non-fungible tokens) are unique valuable virtual assets stored on the blockchain. It can be a piece of art, audio, video, or even a tweet.
- **Stablecoin** - Stablecoin is a cryptocurrency that is backed by a reserve asset that provides price stability. Like a stablecoin of USD will have value almost equal to USD.
- **In-game assets** - Tokens can be used to make tradable in-game assets.

## Token standards in Tezos

The functionality of tokens is defined by some set of rules called token standards. In Tezos, token standards are defined in [TZIPs (Tezos Improvement Proposals)](https://gitlab.com/tezos/tzip). 

There are two token standards on Tezos:

### FA1.2

FA1.2 is an [ERC20](https://eips.ethereum.org/EIPS/eip-20)-like fungible token standard (TZIP-7) for Tezos. At its core, FA1.2 contains a ledger that maps addresses to token balances, providing a standard API for token transfer operations, reading balance, as well as providing approval to external contracts.

<aside>
💡 The FA1.2 specification is described in detail in [TZIP-7](https://gitlab.com/tzip/tzip/blob/master/proposals/tzip-7/tzip-7.md).

</aside>

### FA2

FA2 proposes a unified token contract interface, supporting a wide range of token types including fungible, non-fungible, and semi-fungible tokens. The FA2 provides a standard API to transfer tokens, check token balances, manage operators (addresses that are permitted to transfer tokens on behalf of the token owner) and manage token metadata.

<aside>
💡 The FA2 specification is described in detail in [TZIP-12](https://gitlab.com/tezos/tzip/-/blob/master/proposals/tzip-12/tzip-12.md)

</aside>

> **Note**
FA2 might look like an extended version of FA1.2, but there are some differences. FA2 lacks approvals, which allows you to allow another address to use only some limited amount of your tokens, whereas the operator functionality in FA2 gives them access to all of your tokens. On the other hand, FA2 supports other useful features such as multiple assets and batch transfers.
> 

In the next two sections, you will learn to create your own FA1.2 and FA2 assets on Tezos.
