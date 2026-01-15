+++
title = "Socratic Seminar 20"
date = 2026-01-15
+++

Housekeeping
------------

- This meetup is generously sponsored by Presidio Bitcoin!
- Questions are encouraged, including basic ones!
- Socratic Seminars are held under the [Chatham House Rule](https://www.chathamhouse.org/about-us/chatham-house-rule): share the information you receive, but do not reveal the identity of who said it.
- For the privacy of other attendees, please refrain from taking photographs of other people without their permission.
- Socratic seminars are best when the moderator can let the conversation flow, so try to keep things concrete and focused.
- The reading list covers December 14th, 2025 to January 15th, 2026.

News
----
- [Clarity Act (H.R. 3633)](https://x.com/Jestopher_BTC/status/2011247476095984031)
- [A Mathematical Theory of Payment Channel Networks](https://x.com/renepickhardt/status/2009598480306901363)
- [Lightning Year in Review Stats](https://x.com/ambosstech/status/2007135311558857177)
- [BitGo Adds Support for Lightning Network](https://www.businesswire.com/news/home/20251208754522/en/BitGo-Adds-Support-for-Lightning-Network-from-Custody-Unlocking-Faster-Cheaper-and-Scalable-Bitcoin-Payments)
- [Tether Invests $8M in Speed to Scale Lightning-Based Stablecoin Payments](https://finance.yahoo.com/news/visa-crypto-chief-bets-stablecoin-183008213.html)

bLIPs & BOLTs
-------------
- [Lightning Specification Meeting 2026/01/12](https://github.com/lightning/bolts/issues/1311)

Noteworthy PRs
--------------

### [Core Lightning](https://github.com/ElementsProject/lightning)
- [doc: Update docs to reflect new hsm secret format](https://github.com/ElementsProject/lightning/pull/8838)
- [Askrene: fix infinite cost assertion](https://github.com/ElementsProject/lightning/pull/8832)
- [recovery for modern nodes](https://github.com/ElementsProject/lightning/pull/8830)
- [Modern node hsm_secret fixes](https://github.com/ElementsProject/lightning/pull/8831)

### [eclair](https://github.com/ACINQ/eclair)
- [More tests for accountability](https://github.com/ACINQ/eclair/pull/3240)
- [Rework channel lifecyle events](https://github.com/ACINQ/eclair/pull/3237)
- [Stop storing channel errors in AuditDb](https://github.com/ACINQ/eclair/pull/3236)
- [Don't rebroadcast announcements for spent channels](https://github.com/ACINQ/eclair/pull/3235)
- [Add maxCltvExpiryDelta parameter to findRoute* APIs](https://github.com/ACINQ/eclair/pull/3234)
- [Validate Bolt 11 fallback addresses](https://github.com/ACINQ/eclair/pull/3232)
- [Allow remote dust_limit_satoshis up to 5000 sats](https://github.com/ACINQ/eclair/pull/3227)


### [LDK](https://github.com/lightningdevkit/rust-lightning)


### [lnd](https://github.com/lightningnetwork/lnd)
- [add deprecated no-experimental-endorsement config option](https://github.com/lightningnetwork/lnd/pull/10495)
- [add panic recovery for gossip message processing](https://github.com/lightningnetwork/lnd/pull/10492)
- [fix race condition in link node pruning](https://github.com/lightningnetwork/lnd/pull/10483)
- [enforce non-zero timestamp in gossip messages](https://github.com/lightningnetwork/lnd/pull/10490)
- [use protocol max for fundMax, not maxChanSize](https://github.com/lightningnetwork/lnd/pull/10488)
