---
sidebar_position: 3
---

# Consensus Validator or RPC Node?

Operators who run a consensus validator have much different incentives than operators who run an RPC node.  You will have to decide which choice is best for you based on your interests, technical background, and goals.

## Consensus Validators

As a validator your primary focus is maintaining the network and making sure that your node is performing optimally so that you can fully participate in the cluster consensus.  You will want to attract a delegation of SOL to your validator which will allow your validator the opportunity to produce more blocks and earn rewards.  Each staked validator earns inflation rewards from vote credits. Vote credits are assigned to validators that vote on blocks produced by the leader.  The vote credits are given to all validators that successfully vote on blocks that are added to the blockchain.  Additionally, when the validator is the leader, it can earn transaction fees and storage rent fees for each block that it produces that is added to the blockchain.

Since all votes in Solana happen on the blockchain, a validator incurs a transaction cost for each vote that it makes.  These transaction fees amount to approximately 1.0 SOL per day.  It is important to make sure your validator always has enough SOL in its identity account to pay for the transactions.

There are community provided resources that go into the economics of running a validator.  As an operator, it is important to understand how a validator spends and receives sol through the algorithm.  The following links are a great resource:

*  Congent Crypto has written a [blog post](https://medium.com/@Cogent_Crypto/how-to-become-a-validator-on-solana-9dc4288107b7) that discusses economics and getting started.
* Michael Hubbard wrote an [article](https://laine-sa.medium.com/solana-staking-rewards-validator-economics-how-does-it-work-6718e4cccc4e) that explains the economics of Solana in more depth for stakers and for validators.
* Shinobi Systems created an [economic estimator spreadsheet](https://docs.google.com/spreadsheets/d/1HPU_uG3iJ_ns27CItdWGllW0c-Pn07J0_LEDZs1otQY/edit#gid=0).

For the most up to date resources, go to the [solana discord](https://discord.com/invite/solana) and look in the `#validator-resources` channel for a list of links.

## RPC Nodes

There are different motivations for running an RPC node.  RPC operators do not receive rewards because the node is not participating in voting. Instead, an RPC operator is providing a service to users who want to interact with the Solana blockchain.  Because your primary user is often technical, you will have to be able to answer technical questions about performance of RPC calls.  This option may require more understanding of the core Solana architecture.  You can read more about it in the [Solana docs](https://docs.solana.com/cluster/overview).

If you are operating an RPC node as a business, your job will also involve scaling your system to meet the demands of the users. For example, some RPC providers create dedicated servers for projects that require a high volume of requests to the node. Someone with a background in development operations or software engineering will be a very important part of your team.  You will likely need a good understanding of the Solana architecture and the RPC api.

Alternatively, you may be a development team that would like to run their own infrastructure.  In this case, the RPC infrastructure would likely be a part of your production stack.  A development team could use the [Geyser plugin](https://docs.solana.com/developing/plugins/geyser-plugins) to get real time access to information about accounts or blocks in the cluster.


