# Taquito basics

Taquito is a Javascript/Typescript library for development on the Tezos blockchain.

**Features of Taquito include:**

- Accessing blockchain data
- Injecting transactions into the blockchain
- Originate contracts
- Packing and signing Michelson data

And many more.

> **Note -** This module assumes all the given operations are done with `InMemorySigner` configured (more on that below). Some of the operations will not work with wallets.
> 

## Install

```bash
npm install @taquito/taquito
```

## Reading Balance

```jsx
// import { TezosToolkit } from '@taquito/taquito';
// const Tezos = new TezosToolkit('https://granadanet.api.tez.ie');

Tezos.tz
  .getBalance('tz1h3rQ8wBxFd8L9B3d7Jhaawu6Z568XU3xY')
  .then((balance) => println(`${balance.toNumber() / 1000000} ꜩ`))
  .catch((error) => println(JSON.stringify(error)));
```

## In-memory signer

The `InMemorySigner` package is useful for development and testing. It's an easy way to get started with Tezos when you don't need to interact with a user's wallet. The InMemorySigner is suitable for testing and development.

```jsx
import { TezosToolkit } from '@taquito/taquito';
import { InMemorySigner } from '@taquito/signer';

const Tezos = new TezosToolkit('RPC_URL');

Tezos.setProvider({
  signer: new InMemorySigner('YOUR_PRIVATE_KEY'),
});
```

Now you can use the `Tezos` object to sign operations and inject them into the blockchain.

## Transfer tez

This operation transfers tez to the given address and requires a configured signer.

```jsx
const op = await Tezos.contract
    .transfer({to:address, amount: amount});
await op.confirmation();
console.log("Sent!");
```

## Access Storage

1. **Fetch Contract**
    
    The following code will fetch the contract from RPC. It will be used to interact with your contract.
    
    ```jsx
    // Fetching contract
    const contract = await Tezos.contract.at(CONTRACT_ADDRESS);
    console.log(contract);
    ```
    
2. **Fetch Contract's Storage**
    
    The following code will fetch contract's storage.
    

## Interact with contract

```jsx
// Register here

const contract = await getContract();
const op = await contract.methods.entry_point_name(parameters).send();
console.log(op);
await op.confirmation();
console.log("confirmed!);
```

<aside>
💡 If the contract has single entrypoint, then it is named `default`. Otherwise, in case of multiple entrypoints, they are called with their respective names . Read the content of `contract.methods` from the console for more info.

</aside>

## References

Refer to **[Taquito docs](https://tezostaquito.io/)** to learn more about taquito.

