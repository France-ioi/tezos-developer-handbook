# Wallet integration

[Beacon](https://walletbeacon.io/) SDK is used to connect dApps with wallets. It is the implementation of the wallet interaction standard [tzip-10](https://gitlab.com/tzip/tzip/blob/master/proposals/tzip-10/tzip-10.md).

Developers who plan to develop complex smart contract interactions can use [Taquito](https://github.com/ecadlabs/taquito) with the `BeaconWallet`, which uses this SDK under the hood, but provides helpful methods to interact with contracts.

Besides this Typescript SDK, it also provides SDKs for native iOS and Android Wallets:

- [Beacon Android SDK (Kotlin)](https://github.com/airgap-it/beacon-android-sdk)
- [Beacon iOS SDK (Swift)](https://github.com/airgap-it/beacon-ios-sdk)

## Install

```bash
npm install @taquito/beacon-wallet
```

## Setup

```jsx
import { BeaconWallet } from '@taquito/beacon-wallet';
import { TezosToolkit } from '@taquito/taquito';

const Tezos = new TezosToolkit(RPC_URL);

const wallet = new BeaconWallet({
    name: 'dApp name',
    preferredNetwork: 'granadanet',
    colorMode: 'light'
});

Tezos.setWalletProvider(wallet)
```

## Connect with wallet

You need to get permission from the wallet to connect your dApp with it. 

```jsx
let activeAccount = await wallet.client.getActiveAccount();

// no active account already connected, need permissions first
if (!activeAccount) {
    await wallet.requestPermissions({ network });
    activeAccount = await wallet.client.getActiveAccount();
}
```

Now you can use the `Tezos` object to sign operations and inject them into the blockchain.

## Reading Balance

You can read the balance of any address in the same way as with in-memory signer because it does not require any signer. 

```jsx
Tezos.tz
  .getBalance('tz1h3rQ8wBxFd8L9B3d7Jhaawu6Z568XU3xY')
  .then((balance) => println(`${balance.toNumber() / 1000000} ꜩ`))
  .catch((error) => println(JSON.stringify(error)));
```

## Transfer tez

This operation transfers *****tez* to the given address and requires a configured signer.

```jsx
const op = await Tezos.wallet
    .transfer({to:address, amount: amount});
await op.confirmation();
console.log("Sent!");
```

## Interact with contract

You can interact with a contract in the same way you do with in-memory signer. The only difference is in the contract fetching part. While using wallets, use the `Tezos.wallet` API instead of `Tezos.contract`.

```jsx
// Fetching contract
const contract = await Tezos.wallet.at(CONTRACT_ADDRESS);
console.log(contract);
```

## References

Refer to the below links to learn more about wallet integration.

- [**Wallet API of Taquito**](https://tezostaquito.io/docs/wallet_API)
- **[Beacon docs](https://docs.walletbeacon.io/)**

