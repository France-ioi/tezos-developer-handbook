# Operations

### What are operations on Tezos?

Subsets of operations on Tezos are commonly known as *Transactions,* they usually refer to transfers of tokens or smart contracts calls. 

Some examples of operations which are **not** transactions on Tezos: 

- *Originations*
- E*ndorsements*
- *Proposals*
- *Ballot*

## Implicit accounts and originated accounts

Let's start by talking about the two types of addresses in Tezos:

### I**mplicit account**

- An **implicit account** is linked to a **manager** (see *[General definition of a tezos smart contract*)](https://www.notion.so/Smart-Contracts-Definition-0638d03e305a408c9a579991de12a0ec), which owns the *public key*. The hash of the *public key* outputs an **address**.
- Depending on the chosen **D**igital **S**ignature **A**lgorithm's **e**lliptic **c**urve (see [ECDSA](https://en.wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm)), the latter starts with "***tz1***" (Ed25519 curve), "***tz2***" ([Secp256k1](https://en.bitcoin.it/wiki/Secp256k1) curve), or "***tz3***" (P256 curve).
- In the first *transfer* operation to the account's address, a fixed cost is set aside to create the storage for the account.
- Only *implicit* accounts can be registered as *delegates* and participate in the *baking process*.

### O**riginated accounts**

- **Smart contracts** are also called "**originated accounts**" and are created with an **origination** operation (see *[Smart Contracts](https://www.notion.so/Smart-Contracts-Definition-0638d03e305a408c9a579991de12a0ec)*).
- They don't have a private key and public key pair. Originated accounts' addresses start with ***KT1***. They run their Michelson code each time they receive a transaction.

## Tezos operations

An operation is usually a *message* sent from one address to another.

Message representation:

type operation = {
amount: amount; // amount being sent
parameters: data list; // parameters passed to the script
counter: int; // invoice id to avoid replay attacks
destination: contract hash;
}

### Writing Smart Contracts

- [Example of an Entrypoint call](https://www.notion.so/Writing-Smart-Contracts-7d3b6ffbf5b546b5baf5071bf84a16f7)

## Operation Flow

- [Deploying Smart Contracts](https://www.notion.so/Deploying-and-interacting-with-smart-contracts-7652d420c6474cc88696b5139eeba344)

The diagram below represents the life cycle of an operation:

![https://opentezos.com/assets/images/operation_flow-7e54b4bc312856ddd81318ee6789daf9.svg](https://opentezos.com/assets/images/operation_flow-7e54b4bc312856ddd81318ee6789daf9.svg)

FIGURE 1: Life cycle of an operation

Source: OpenTezos

Nodes receive operations from clients via RPC or from a peer in the network. Note that this is how a typical Tezos node works on protocol "*Alpha*".