# SmartPy Cheatsheet

This cheat sheet is a quick reference for developing smart contracts. 

If you are completely new to SmartPy, then you should definitely check our **[Quick Start](https://www.notion.so/Overview-e057760f88b04031893ae82e3c8d505b)** section.

# Table of contents

- **[SmartPy](https://www.notion.so/SmartPy-Cheatsheet-c9d12639a93a436e9d76cd0b664e6079)**
- **[Basic Template](https://www.notion.so/SmartPy-Cheatsheet-c9d12639a93a436e9d76cd0b664e6079)**
- **[Data Types](https://www.notion.so/SmartPy-Cheatsheet-c9d12639a93a436e9d76cd0b664e6079)**
- **[Commonly Used functionalities](https://www.notion.so/SmartPy-Cheatsheet-c9d12639a93a436e9d76cd0b664e6079)**

# SmartPy

[SmartPy](https://smartpy.io/) is an intuitive and powerful smart contract development platform for Tezos.

The SmartPy code is compiled down to **Michelson** - a domain-specific low-level programming language for smart contract development on Tezos.

<aside>
💡 SmartPy has well-written documentation. Do go through it [here](https://smartpy.io/docs/).

</aside>

# Basic Template

```python
import smartpy as sp

class ExampleContract(sp.Contract):
    def __init__(self, value):
				# initializing contract storage
        self.init(
            storedValue = value,
        )

    @sp.entry_point
    def update(self, params):
        # setting params type (optional but recommended :) )
        sp.set_type(params, sp.TRecord(
            value = sp.TNat,
        ))
            
        # Store a new value
        self.data.storedValue = params.value

@sp.add_test(name = "Example Contract")
def test():
		# creating test_scenario
    scenario = sp.test_scenario()
		# initialsing contract
    c1 = ExampleContract(1)
    scenario += c1
		# calling entry point
    c1.update(value = 2)

# A a compilation target (produces compiled code)
sp.add_compilation_target("my_contract_compiled", ExampleContract(value = 0))
```

# Data types

[Types](https://www.notion.so/15db98e8c5b743b4bfe16fbfbe44ca3d)

> **Note**
> 
- All data types in Michelson (so in SmartPy too) are unbounded. So for example, there is no maximum value for numbers. These are like BigInt / BigNumber in other languages.

# Commonly used functionalities

### `sp.sender`

Tells the address of the sender of the current operation. It can be used for authentication purposes. It is secure as the operation is signed with the private key of the sender.

### `sp.amount`

Tells the amount of current transaction which is of type `sp.TMutez`.

### `sp.balance`

Tells the balance of the contract in `mutez`.

### `sp.send`

`sp.send(destination, amount, message = None)`

It sends specified amount to the destination contract.

## Verify conditions

### `sp.verify(condition, message = "")`

Used to check the validity of a condition. It terminates and rollbacks the whole transaction if it fails with `message` as an error message.

It can be used to restrict access to an entrypoint. For example, in an NFT contract only admin should be able to mint. To ensure this following statement is used.

`sp.verify(self.data.admin == sp.sender, message = "NOT_ADMIN")`

### `sp.fail_with("message")`

It aborts the current transaction and raises a message.

## Local variables

### `sp.local`

It is used to create local variables in SmartPy. It is defined as follows.

`x = sp.local('x', sp.nat(0))`

Its value can be accessed by `x.value`.

Its value can be updated by `x.value = 10`.

<aside>
⚠️ `sp.local` is crucial to create local variables in SmartPy.
Normal pythonic assignment of some value or expression to an identifier only creates an alias, not a variable.
For example,
`x = sp.nat(10)` will set `x` as an alias for `sp.nat(10)`. Assigning it some other value later will have unexpected results

</aside>

## Conditional statements

### `sp.if` & `sp.else`

These are conditional statements that are evaluated on-chain.

<aside>
💡 Michelson, and hence SmartPy, does not have any "else if" statement.

</aside>

<aside>
⚠️ `sp.if` is different from `if`. `sp.if` are evaluated on-chain, whereas `if` statement is evaluated on compilation (this is called metaprogramming). Be sure to use `sp.if` for contract logic. You can see the difference in the compiled output.

</aside>

## Loops

### `sp.for`

A for loop that is evaluated on-chain. It can be used to iterate through the values of a list or set, or keys of a map.

### `sp.while`

A while loop that is evaluated on-chain. It is generally used with local variables to iterate a fixed number of times.

## Int vs Nat conversions

### `sp.as_nat()`

Converts `int` to `nat`.

### `sp.to_int()`

Converts `nat` to `int`.

## Setting data types

### `sp.set_type`

It is used to set the data type of parameters of an entry point.

```python
@sp.entry_point
def update(self, params):
    sp.set_type(params, sp.TRecord(
        id = sp.TNat,
        value = sp.TNat,
    ))
```

## Block info

### `sp.now`

Tells the timestamp of the current block. Useful to know the time of execution of the current transaction

### `sp.level`

Tells the current block level.

## References

- SmartPy Docs: [https://smartpy.io/docs](https://smartpy.io/docs)
- SmartPy IDE: [https://smartpy.io/ide](https://smartpy.io/ide)
- In case of doubts, ask here: [https://t.me/SmartPy_io](https://t.me/SmartPy_io)
