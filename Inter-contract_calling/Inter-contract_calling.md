# Inter-contract calling

Inter-contract calling means invoking an entrypoint of a smart contract from another smart contract.

It has a lot of use cases, from handling [FA](https://www.notion.so/Glossary-e9a82a9d0faa4d279ecee6faa6b3e7c5) tokens to accessing off-chain data using oracles.

For creating an inter-contract call, follow the steps below:

## Define the recipient contract

```python
contract = sp.contract(
    <data_type>, <contract_address>, <entry_point_name>
).open_some("Invalid contract")
```

`sp.contract` is used to define the particular entrypoint of a contract that you want to call. It takes in three parameters:

- `data_type` - It is the data type of parameters of the recipient entrypoint.
- `contract_address` - Address of the recipient contract.
- `entry_point_name` - The name of the entrypoint to call.

`sp.contract` returns an [option](https://www.notion.so/Option-3704f97509d443139ff6b692ed6d8aa5) object. On calling `open_some("Error message")`, it returns the contract object or throws an error with an optional error message, in case the parameters are invalid.

Here's an example of calling the transfer method of an FA2 contract:

```python
data_type = sp.TList(
    sp.TRecord(
        from_ = sp.TAddress, 
        txs = sp.TList(
            sp.TRecord(
                amount = sp.TNat,
                to_ = sp.TAddress,
                token_id = sp.TNat
            ).layout(("to_", ("token_id", "amount")))
        )
    ).layout(("from_", "txs"))
)

contract = sp.contract(data_type, FA2_token.tokenAddress, "transfer").open_some()
```

## Set the data to be sent

Set the data to be sent as a parameter in the contract call. This data should be of the same type as defined in the previous step.

Here's an example for setting data to be sent of an FA2 contract.

```python
data_to_be_sent = sp.list([
    sp.record(
        from_ = sp.sender, 
        txs = sp.list([sp.record(
            amount = deposit.value,
            to_ = sp.self_address, 
            token_id = FA2_token.tokenId
        )])
    )
])
```

## Execute the call

```python
sp.transfer(<data_to_be_sent>, <amount>, <contract>)
```

`sp.transfer` is used to execute the call. It requires the following parameters:

- `data_to_be_sent` - It is the data that is to be sent as the parameter of the recipient entrypoint.
- `amount` - The amount of *tez* to send along with the contract call.
- `contract` - The contract object containing the contract address and name of the recipient entrypoint.

Finally, for sending a contract call with a 0 [mutez](https://www.notion.so/Glossary-e9a82a9d0faa4d279ecee6faa6b3e7c5) amount:

```python
sp.transfer(data_to_be_sent, sp.mutez(0), contract)
```

## References

For learning more about **Inter-contract calls** refer [here](https://cryptocodeschool.in/tezos/academy/module-02).

Docs: [https://smartpy.io/docs/types/contracts_addresses/#transfer](https://smartpy.io/docs/types/contracts_addresses/#transfer)

