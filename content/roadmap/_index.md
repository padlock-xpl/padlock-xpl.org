---
title: "Roadmap"
description: "The path to PADLOCK's mainnet release"
---

These are all the things that need to be accomplished before PADLOCK's initial
release. Development is very early right now.

# UTreeXO implementation
[UTreeXO](https://dci.mit.edu/utreexo) allows the entire UTXO set to be
represented in under a kilobyte. When implemented on Bitcoin, running a fully
validating node takes only a few gigabytes.

On PADLOCK, UTreeXO will not only significantly reduce the overhead of storing
and validating transactions, it's also what allows UTXO set sharding to work.

#### State of Development
Not started


# Proof of Staked Work implementation
Proof of Staked Work (PoSW) is a consensus mechanism designed to use very little
electricity and lower the barrier to entry of participating in block production.
This is achieved by only mining a proof of work block every 50 blocks, then
adding that block's miner to the set of available block producers. For all the
non proof of work blocks, a block producer is chosen through the set of previous
block miners at random

#### State of Development
Not started


# Peer to Peer Protocol
The protocol used to communicate between peers.

#### State of Development
Not started


# Single shard testnet
This testnet will allow for real world testing and benchmarking of UTreeXO and
PoSW.

#### State of Development
Not started


# UTXO set sharding
UTXO sharding allows for nodes to only store a small portion of the UTXO set.
This would allow for the storage of UTreeXO merkle proofs to be decentralized
and make it so users would not have to rely on a higher class of node that
stores the UTXO set. However, it is even possible to fully validate the chain
without storing any of the UTXO set, and only a small (<1 kilobyte) amount of
data, thanks to UTreeXO.


# Single shard mainnet
Whether or not mainnet will be released as a single shard initially is unsure.
It depends on the demand for PADLOCK at the time.

#### State of Development
Not started

# Fraud proofs
Fraud proofs allow for a node to prove to the rest of the network that a block
is invalid. This is integral to PADLOCK's sharding model, as it allows nodes to
only validate part of a block and be sure that the rest is valid.

#### State of Development
Not started


# Data availability proofs
Data availability proofs allow for a prover to prove to a verifier that some
piece of data is available without disclosing the entire piece of data. This is
needed for sharding in PADLOCK, because fraud proofs cannot be generated for
data that doesn't exist.

#### State of Development
Not started


# Confidential Transactions
Confidential transactions allow the amounts in a transaction to be hidden, well
still allowing verification of zero balance sums.

#### State of Development
Not started
