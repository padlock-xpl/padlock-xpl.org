---
title: "About"
---
PADLOCK is a highly scalable and decentralized blockchain protocol. For users
this means low fees even when the network is under use. For anyone who wants to
run a validating node, or produce blocks, this means that the overhead of
running a node is low, despite PADLOCK providing very high throughput.

PADLOCK's whitepaper can be found
[here](https://github.com/padlock-xpl/padlock-whitepaper)

PADLOCK utilises various techniques such as sharding, UTreeXO, UTXO expiry, UTXO
commitments and Proof of Staked Work to allow for very high throughput and low
fees, well still remaining decentralized.

# Sharding
PADLOCK allows for sharded block verification, which makes running a validating
node very easy. If nodes detect fraud in their shard, they can alert the rest of
the network with a fraud proof. PADLOCK also shards the UTXO set.

# UTreeXO
[UTreeXO](https://dci.mit.edu/utreexo) allows the entire UTXO set to be
represented in under a kilobyte. It also makes validating transactions far
quicker, and cut sync time by 60%.

# UTXO Expiry
Sometimes UTXOs are sent to invalid addresses, or addresses for which the
private key is lost. Or, perhaps the UTXO isn't going to be spent for a long
time. In order to reduce the cost of storing these UTXOs, old UTXOs are made
unspendable, and nodes will stop storing them. However, they can be reintroduced
by providing a proof of their existence before being expired.

# UTXO Commitments
UTXO commitments remove the requirement for nodes to sync from the very
beginning of the blockchain. Node operators can choose how far back they want to
sync from, and be sure beyond any reasonable doubt that they have downloaded the
correct UTXO set.

# Proof of Staked Work
Proof of Staked work is a novel consensus mechansim designed to use less energy,
and lower the barrier to entry of becoming a block producer.
