# History of amendments

## [Athens](https://www.tezosagora.org/proposal/1) (Pt24m4xiP)

*Athens* was the first proposed protocol-amendment for Tezos. Two proposals - [Athens A](https://www.tezosagora.org/proposal/1) and [Athens B](https://forum.tezosagora.org/t/athens-b-psd1ynubh/33) - were proposed by [Nomadic Labs](https://blog.nomadic-labs.com/athens-our-proposals-for-the-first-voted-amendment.html) in February 2019.

Of the two proposals, *Athens A* sought to increase the gas limit and reduce the required roll size for baking from 10,000 tez to 8,000 tez. *Athens B* only sought to increase the gas limit. Athens A was voted with a *Super-majority* and was autonomously [activated](https://twitter.com/TezosAgoraBot/status/1133901612790034432?s=20) into the protocol in May 2019.

For a full list of changes, be sure to read this corresponding blog [post](https://blog.nomadic-labs.com/athens-proposals-injected.html) from Nomadic Labs and [reflections](https://medium.com/tqtezos/reflecting-on-athens-the-first-self-amendment-of-tezos-4791ab3b1de1) by Jacob Arluck.

## [Brest A](https://www.tezosagora.org/proposal/3) (PtdRxBHv)

*Brest A* was the first proposed amendment rejected during the *Exploration Period*. Submitted in June 2019, it received only 0.35% of the votes during the *Proposal Period*. But as it had no competition, the system promoted it. The amendment was then rejected in the *Exploration Period* with only 0.26% of favourable votes. The 80% *Super-majority* was not reached, neither was the minimum *Quorum* required to validate it.

This proposal would have fixed a security breach linked to the rehashing push during the *Athens* protocol change. Moreover, it would have facilitated the amendment's invoice tracking. But the invoice for this proposal, 8,000 tez, was much higher than the usual cost.

## [Babylon](https://www.tezosagora.org/proposal/5) (PsBABY5nk)

The *Babylon* proposal was composed of two proposals made in July/August 2019: [Babylon](https://www.tezosagora.org/proposal/4) and [Babylon 2](https://www.tezosagora.org/proposal/5). *Babylon 2* was built by Nomadic Labs, Cryptium Labs (Metastate), and Marigold, after receiving feedback on the first *Babylon* proposal. The teams proposed a new tweaked version in the same proposal period.

Notable changes included a new variant of the consensus algorithm (`Emmy+`). There were new Michelson features and accounts rehaul to aid smart contract developers. The accounts rehaul enabled a clearer distinction between "*tz*" and "*KT*" addresses. Furthermore, there was a refinement of the Quorum formula and the addition of the 5% threshold.

Babylon was autonomously [activated](https://twitter.com/adrian_brink/status/1185137422432161792?s=20) into the protocol in October 2019.

For a full list of changes, be sure to read the corresponding blog posts from [Nomadic Labs](https://blog.nomadic-labs.com/babylon-proposal-injected.html), and [Cryptium Labs](https://medium.com/metastatedev/on-babylon2-0-1-58058d9d2106) (Metastate).

## [Carthage](https://www.tezosagora.org/proposal/6) (PtCarthav)

*Carthage* was the first proposal to be rejected during the *Proposal Period*. Since the *Babylon* change, it now took a minimum of 5% approval to move to the *Exploration Period* and *Carthage* only obtained 3.5%.

The purpose of this proposal was to increase the gas limit per block and per operation by 30% to improve the accuracy of the existing formula used for calculating baking, endorsing rewards, and to fix various minor issues.

## [Carthage 2.0](https://www.tezosagora.org/proposal/7) (PtCarthav)

*Carthage 2.0* was then proposed and overwhelmingly accepted in December 2019 partly due to the Nomadic Labs and Cryptium Labs (Metastate) contributions.

Notable changes included increasing the gas limit per block and per operation by 30%, improving the accuracy of the formula used to calculate baking and endorsing rewards, as well as several minor improvements to Michelson. The main difference with *Carthage* was the new and more secure formula to calculate rewards.

*Carthage 2.0* was autonomously [activated](https://twitter.com/tezos/status/1235590757416751105?s=20) onto the protocol in March 2020.

For a full list of changes be sure to read the corresponding [changelog](https://tezos.gitlab.io/protocols/006_carthage.html#changelog) and blog posts from [Nomadic Labs](https://blog.nomadic-labs.com/carthage-changelog-and-testnet.html) and [Cryptium Labs](https://medium.com/metastatedev/updating-the-potential-carthage-proposal-and-resetting-the-carthagenet-test-network-f413a792571f) (Metastate).

## [Delphi](https://www.tezosagora.org/proposal/8) (PsDELPH1K)

The *Delphi* proposal was a Nomadic Labs, Metastate, and Gabriel Alfour contribution, adopted in September 2020.

Notable changes included improving the performance of the Michelson interpreter, improving gas costs by adjusting the gas model, reducing storage costs by 4 times, and various minor fixes.

*Delphi* was autonomously [activated](https://twitter.com/tezos/status/1326877616322859009?s=20) into the protocol in November 2020.

For a full list of changes, be sure to read the corresponding [changelog](https://blog.nomadic-labs.com/delphi-changelog.html#007-delphi-changelog) and blog post from [Nomadic Labs](https://blog.nomadic-labs.com/delphi-official-release.html).

## [Edo](https://www.tezosagora.org/proposal/9) (PtEdoTezd)

The *Edo* proposal was adopted in November 2020 with Nomadic Labs, Metastate, and Gabriel Alfour contributions.

Edo added two major features to Tezos smart contracts:

- *Sapling*[[1]](https://opentezos.com/tezos-basics/history-of-amendments#references) and *BLS12-381*[[2]](https://opentezos.com/tezos-basics/history-of-amendments#references) to enable privacy-preserving smart contracts
- *Tickets*[[3]](https://opentezos.com/tezos-basics/history-of-amendments#references) for native on-chain permissions and assets issuance.

Among other features, Edo also updated the Tezos amendment process by lowering period length to 5 cycles and by adding a 5th *Adoption Period*. A full changelog is available [here](https://tezos.gitlab.io/protocols/008_edo.html).

## [Florence](https://www.tezosagora.org/proposal/11) (PsFLorena)

The *Florence* proposal was a joint effort from Nomadic Labs, Marigold, DaiLambda, and Tarides.

Florence's notable bug fixes and improvements are the:

- Increasing maximum operation size
- Improved gas consumption for the execution of more complex smart contracts
- Changing inter-contract calls to a depth-first serach[[4]](https://opentezos.com/tezos-basics/history-of-amendments#references) ordering, as opposed to breadth-first search[[5]](https://opentezos.com/tezos-basics/history-of-amendments#references) ordering
- The elimination of the test chain activation

*Bakings Accounts*[[6]](https://opentezos.com/tezos-basics/history-of-amendments#references) was also included in the feature set. However, ongoing testing uncovered some important and previously undocumented breaking changes in the proposal with *Baking Accounts*. Hence, the feature was postponed until a thorough audit of the functionality was completed or that an alternative implementation was produced. The version of *Florence* without *Baking Accounts* was considered a safer choice.

## [Granada](https://forum.tezosagora.org/t/announcing-granada/3183)

The Granada update contains several improvements to the protocol with numerous bug fixes and minor improvements:

- Emmy* — Replacing the current Emmy+ proposal with Emmy* which will halve the time between blocks from 60 seconds to 30 seconds and allow transactions to achieve significantly faster finality than under the current consensus mechanism
- Liquidity Baking — Piggybacking off liquidity and global availability of Bitcoin, and incentivizing large amounts of decentralized liquidity provision between tez and wrapped bitcoins
- Gas improvements — Observed a decrease of a factor of three to six in the gas consumed in the execution of already deployed contracts. This will allow developers to deploy richer, more complicated, and more interesting applications on Tezos at reasonable real-world cost

The complete changelog can be viewed [here](https://tezos.gitlab.io/protocols/010_granada.html)

## [Hangzhou](https://forum.tezosagora.org/t/announcing-tezos-8th-protocol-upgrade-proposal-hangzhou/3695)

The Hanzhou upgrade has been accepted by the Tezos community and was activated at approximately 16:20:22 UTC on December 3rd, 2021

Some of the most interesting and important changes:

- Timelock — Timelock encryption makes it possible for smart contract authors to include strong countermeasures against Block Producer Extractable Value (referred to as “MEV” on proof-of-work chains)
- Views — A new kind of entrypoints in smart contracts which makes internal state information more easily accessible to other smart contracts
- Cache — Provides faster access to regularly accessed data and lowers the gas cost associated with it. This directly increases the throughput of Tezos and can be built upon to further improve the performance of various parts of the protocol
- Global Table of Constants — Allow smart contract developers to register Michelson expressions as “constants” and reference them in contracts
- Context Flattening — Rewriting of the protocol’s database internals to optimize storage use and also enable future optimisations to speed up the processing of blocks and operations
- Liquidity baking — Small increase to liquidity baking sunset level. Without this, the subsidy would halt during the lifespan of this protocol

The complete changelog can be viewed [here](https://tezos.gitlab.io/protocols/011_hangzhou.html)