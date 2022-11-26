# Liquid Proof-of-Stake (LPoS)

### Proof Of Stake (PoS)

Instead of using highly energy-intensive mining equipment and hardware to validate transactions, the Proof-of-Stake consensus mechanism requires miners to stake all or a portion of their coins in order to be eligible to validate transactions. The validators are chosen to verify a block randomly but those who have a larger stake or have been staking longer have an advantage. 

A staking mechanism, a weighted amount of financial collateral a node commits to the network, is used in PoS instead of hashing power in PoW.

Any participant can stake the native token on the network, in which you can be part of the staking pool or in control of the staking pool entirely if you meet the full requirements to be a full-fledged validator. 

PoS algorithms use several methods to select which nodes will validate transactions:

- **The size of the stake**: the more tokens staked, the higher the chance of being selected to validate the next block.
- **The age of the tokens staked**: the longer the tokens have been unspent, the higher the chance of being chosen to validate the next block.
- **Random selection**: While the PoS validator selection process is tilted in favor of larger token holders, this mechanism is still embedded with a degree of randomness in order to avoid centralization.

Computational power in PoW systems requires mining hardware to expend energy in competition with one another. Therefore by eliminating this need for energy-intensive mining hardware, PoS is typical a far more resource-efficient consensus mechanism system compared to PoW blockchains as the PoS’s pseudo-random selection process is mainly based on passive crypto deposits rather than computational power.

Since these technical barriers in which equipment was required to participate in the network. PoS opened more opportunities and possibilities for anyone to participate in a network’s validation process. Thus lowering the bar for access results in greater decentralization as nodes are distributed more widely and thus increasing security for the blockchain network.

## Liquid Proof of Stake(LPoS)

Tezos has developed Liquid Proof of Stake(LPoS), an evolution of PoS idea.

Validators in Tezos’s LPoS are called "**bakers**" or "**endorsers**". Any user can become a validator if he has enough tez. Tezos allows users the **choice** to ***delegate** if they don’t have enough coins*. 

Diluting the activity and increasing inclusion is Tezos’ idea to promote governance *liquidity* rather than the network's *scalability*. The two roles of delegates are simple:

- Bakers: creating and signing blocks
- Endorsers: approving blocks by issuing an endorsement operation (endorsements visible at the block level `n + 1` relate to the block level `n`).

The quantity of tez to bake or endorse is an important parameter. Increasing the amount will discourage Sybil attack or 51% attack, decreasing it to coordinate cartels or coalitions dissolutions.

Currently, a validator needs 8,000ꜩ (one "*roll*") to take part in the consensus (lowering the limits of these validators can be proposed in future upgrades to the protocol). However, similar to DPoS, the reward probability is still proportional to the invested amount. 

The baking time has cycles, and the tokens are still frozen as bonds during this process.