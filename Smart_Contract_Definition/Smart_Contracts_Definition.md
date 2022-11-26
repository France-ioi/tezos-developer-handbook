# Smart Contracts Definition

## General definition of a Smart Contract

Smart contracts are programs that are stored on a blockchain and run when predetermined conditions are met. Smart contracts are typically used for the automation of the execution of the agreement or condition. This ensures that all participants can be immediately certain of the outcome, without an intermediary’s involvement or time loss. They can also automate a workflow, triggering the next action when conditions are met.

## **Tezos Smart Contract**

Tezos smart contracts are stored on the Tezos blockchain. They contain a set of rules and instructions which can be triggered by users or another piece of code. It is deployed using an “operation” onto the blockchain, where it stays immutable and publicly verifiable to everyone.

Since the smart contract is immutable so is the instructions and the rules inside it, the key difference being with a transfer of coins is a user *can trigger the execution of the code without modifying it.*

### **Operations for Smart Contract**

Different from Bitcoin, which uses UTXO model to record the transaction receipt, Tezos uses a stateful account model to record the balance of an account [[1]](https://opentezos.com/tezos-basics/smart-contracts#references).

Tezos accounts fall in either of these 2 categories:

1. Classic accounts with a primary address, to store tez (ꜩ)
2. Smart contract accounts with an address, storing code and tez (ꜩ)

"C*ontracts*" usually refers to both types in general. 

- Every c*ontract* has a "***manager***".
- Classic account has an "***owner***".

If a contract has the "*spendable*" property, the manager is the entity allowed to spend funds from it.

The functions of a smart contract can trigger different kinds of operations. Take for example of a vending machine dispensing multiple items:

- The machine will need a contract to govern the quantity for exchange with the user interacting with it. *Give me a dollar in exchange for one bottle of water.*
- The machine can also have different smart contracts for each item it stores or a single smart contract that governs the transaction of all the items in it.
- The contract in the machine will also be liable for keeping track of the amount of supply for each item and the display on the machine (front-end) will interact with the contract to fetch and display that amount to users.

Nothing can be retrieved from the vending machine unless the right conditions are met (sufficient amount inputted) and triggered by the user (selecting his/her choice). 

### **Code is Law**

Smart contracts allow an **agreement** to be secured between two or more parties. In this context, the concept of "[Code is Law](https://en.wikipedia.org/wiki/Lawrence_Lessig#%22Code_is_law%22)" from *[Lawrence Lessig](https://en.wikipedia.org/wiki/Lawrence_Lessig)* is very appropriate. 

Smart contracts can be used to create financial instruments like various *tokens* (usually worth a fraction of the blockchain's *coin*) with different usability and characteristics inside a multiple smart contracts system. 

### **How does Smart Contracts benefits Society?**

- Smart contracts allow developers to create strict rule-based decisions in code that can facilitate protocols that require them such as *lending*, *stablecoins*, or *crowdfundings*.
- In most cases, smart contracts remove *intermediates* and drastically reduce costs compared to classic paper contracts and their validations.

Notice that like any other, a Tezos smart contract can only run and interact with the blockchain it's stored on. It can't interact with other networks. However, that's where *decentralized applications* or "*Dapps*" come in because they provide interfaces for the outside world.

### Lifecycle of a Tezos smart contract

Smart contracts on Tezos can be deployed once but can be called upon many times. They can also interact with each other through inter-contract calls as well as communicate with data outside of the blockchain through [Oracles](https://tezos.b9lab.com/oracles). 

Lifecycle Steps of a Tezos Smart Contracts include:

1. Deployment
2. Interactions through calls

### Deployment of a Tezos smart contract

**“Origination”** is the name for the deployment of a Tezos smart contract.

When the smart contract is deployed, an **address** and a corresponding *persistent space* called "**storage**" are allocated to this smart contract. Storage of the smart contract defines its usable space and address is the location and identity of where it is stored on the Tezos blockchain.

Once deployed, anyone can call the smart contract (e.g. other contracts) with an *operation* (see more about them in the *[Operations](https://opentezos.com/tezos-basics/operations)* chapter) sent to its address with arguments. Thus, calling this smart contract triggers the execution of the set of pre-defined instructions.

### **Origination**

The origination of a Tezos smart contract must define:

- A complex **Parameter Type**
- **Storage Type**
- **Set of instructions** in the low-level *Michelson* language

### CLI command

The CLI command "`tezos-client originate`" can be used to deploy a Tezos smart contract. Arguments are the following:

- Name of the smart contract
- Michelson script containing:
    - Parameter Type
    - Storage Type
    - Set of instructions
- Initial storage value
- Amount of tez sent to the smart contract
- An optional address of a delegate

The command returns the newly deployed contract's address (more detail in the ["*CLI and RPC*"](https://opentezos.com/tezos-basics/cli-and-rpc) chapter).