---
title: "Comparing PADLOCK to Other Blockchains"
author: "Ellis Frank"
date: "2021-07-24"
---

What makes PADLOCK different than other blockchains?

# Bitcoin Core
Bitcoin Core has given up on any sort of on-chain scaling. It has a theoretical
cap of 7 transactions per second, but in practice, that is more like 3. The hope
is that Bitcoin can scale with the lightning network. However, the lightning
network has many issues. First, the user experience is generally bad with
non-custodial wallets. Setting up channels is a tedious process, especially for
new users. Setting up a channel also requires an on-chain transaction, which can
cost a lot in fees. It's also recommended to have many channels in order to help
decentralization, which requires even more fees to be paid. It's also not even
just a one time payment, as channels will need to be balanced sometimes.

Second, it doesn't really scale well remaining decentralized. There is a pretty
convincing [proof that lightning can't scale well remaining decentralized
](https://medium.com/@jonaldfyookball/mathematical-proof-that-the-lightning-network-cannot-be-a-decentralized-bitcoin-scaling-solution-1b8147650800).
It would result in an easily regulated class of supernodes. Not great for
censorship resistance.

Third, in order for lightning to scale, Bitcoin Core would need a block size
increase. To onboard everyone in the US with just one channel would take nearly
3 and a half years (`330,000,000 / 3 tps / 60 seconds in a minute / 60 minutes
in hour / 24 hours in days / 365 days in year = 3.49`). Also, sometimes channels
will need to be rebalanced, which creates more transactions. This also is
assuming no other transactions are being made. You'll also need to open more
than one channel most likely. With four channels (which is on the low side) it'd
take 14 years (`3.49 * 4 = 13.96`)

PADLOCK aims to scale on-chain, which is much simpler and doesn't result in a
special and easily regulated class of supernodes, like lightning does.


# Bitcoin Cash
Bitcoin Cash forked off from Bitcoin around mid-late 2017, in order to raise the
block size limit. The argument against raising the block size cap is that it
would make running a full node too hard, thus meaning there would be
centralization of nodes.

I generally agree with the sentiment, but you have to find a good balance
between letting many users run a full node and allowing the network to actually
function. I personally think that 32 megabyte blocks is a perfectly good
balance, and could probably be increased more well still being accesible to a
large amount of users.

Both versions of Bitcoin tend to ignore the centralization of block production
though. Becoming a Bitcoin miner requires dumping >5000$ on specialized mining
hardware. This has resulted in the distribution of new coins being very
centralized, as well as easier censorship. There is already such thing as
[compliant
mining](https://news.bitcoin.com/marathon-mines-first-ofac-compliant-bitcoin-block/).

Bitcoin Cash aims to scale by optimizing a single shard as much as possible.
This does work, but isn't really sustainable. You can only optimize the software
so much. The common counter to this is that by the time BCH gets large scale
adoption, hardware will have improved a lot. It is probably true that hardware
will have improved, but transaction demand could easily increase a lot by then
as well. 


# Ethereum
Ethereum is a general purpose blockchain, whereas PADLOCK is just meant to run
one currency, XPL. PADLOCK just has one purpose (a currency) to allow for more
optimizations for that one purpose.

PADLOCK and Ethereum both plan on using some form of sharding. Ethereum, though,
is only going to do Data Sharding, and then might do Execution sharding later
on. PADLOCK plans on doing both. This is a much easier thing to do on PADLOCK
than Ethereum, due to PADLOCK using a UTXO system, and being far more simple
(no Virtual Machine, etc).

Ethereum plans on scaling with layer 2 solutions, whereas PADLOCK does not.
Rollups are great scaling tech, and PADLOCK actually functions in a very similar
way to optimisic rollups, where data (in PADLOCK's case, only data from shards
the node doesn't validate) is considered valid until a fraud proof is generated
on it.
