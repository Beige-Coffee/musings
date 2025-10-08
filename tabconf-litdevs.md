+++
title = "TABConf Socratic Session: Lightning BOLT Spec and Implementation Updates"
date = 2025-10-16
+++

Housekeeping
------------

- Questions are encouraged, including basic ones!
- Socratic Seminars are held under the [Chatham House Rule](https://www.chathamhouse.org/about-us/chatham-house-rule): share the information you receive, but do not reveal the identity of who said it.
- For the privacy of other attendees, please refrain from taking photographs of other people without their permission.
- Socratic seminars are best when the moderator can let the conversation flow, so try to keep things concrete and focused.
- Today's focus is Lightning BOLT Spec and Implementation Updates

News
----
- [Lightning++ Happened!](https://btcpp.dev/conf/berlin25)
- [Lightning Specification Meeting 2025/10/06](https://github.com/lightning/bolts/issues/1293)

Zero-Fee Commitments
----
#### BOLT
- [Zero-fee commitments using v3 transactions (feature 40/41) ](https://github.com/lightning/bolts/pull/1228)
#### Implementations
- Core Lightning
- Eclair
- LDK
  - [LDK High Level Tracker](https://github.com/lightningdevkit/rust-lightning/issues/3789)
- LND
  - [[feature]/sweeeper: add P2A + Ephemeral Dust awareness to BumpFee command](https://github.com/lightningnetwork/lnd/issues/9778)
  - [[feature]: Zero Fee Commitments](https://github.com/lightningnetwork/lnd/issues/10201)

Simple Taproot Channels
----
#### BOLT
- [extension-bolt: taproot gossip (features 32/33)](https://github.com/lightning/bolts/pull/1059)
#### Implementations
- Core Lightning
- Eclair
  - [Eclair v0.13.0 release contains initial implementation of taproot channels](https://github.com/ACINQ/eclair/releases/tag/v0.13.0)
  - [Roadmap for new commitment formats and old commitment formats clean-up](https://github.com/ACINQ/eclair/issues/3059)
  - [Simple taproot channels](https://github.com/ACINQ/eclair/pull/3103)
- LDK
  - [High Level Tracker](https://github.com/lightningdevkit/rust-lightning/issues/2295)
    - Is this still acurrate?
- LND
  - [Release Notes 0.17.0](https://github.com/lightningnetwork/lnd/blob/master/docs/release-notes/release-notes-0.17.0.md)
 
(Taproot) Gossip V2
----
#### BOLT
- [extension-bolt: taproot gossip (features 32/33)](https://github.com/lightning/bolts/pull/1059)
#### Implementations
- Core Lightning
- Eclair
- LDK
- LND
  - [[epic]: Gossip 1.75](https://github.com/lightningnetwork/lnd/issues/7961)


Splicing
----
#### BOLT
- [Channel Splicing (feature 62/63)](https://github.com/lightning/bolts/pull/1160)
- [BOLT 2: quiescence protocol (feature 34/35) option_quiesce](https://github.com/lightning/bolts/pull/869)

#### Implementations
- Core Lightning
  - [Splice: Interop Final (probably) with Eclair](https://github.com/ElementsProject/lightning/pull/8021)
  - [splicing: Adds the features needed to enable collaborative splicing & resizing of active channels](https://github.com/ElementsProject/lightning/pull/6253)
- Eclair
  - [Simple taproot channels & splicing](https://github.com/ACINQ/eclair/pull/3103)
  - [Send channel_announcement for splice transactions on public channels](https://github.com/ACINQ/eclair/pull/2968)
  - [Implement on-the-fly funding based on splicing and liquidity ads](https://github.com/ACINQ/eclair/pull/2861)
  - [Add support for RBF-ing splice transactions](https://github.com/ACINQ/eclair/pull/2925)
  - [Add quiescence negotiation](https://github.com/ACINQ/eclair/pull/2680)
  - [Add support for splices](https://github.com/ACINQ/eclair/pull/2584)
- LDK
  - [Add splice-out support](https://github.com/lightningdevkit/rust-lightning/pull/3979)
  - [Simplify Quiescence and prepare for splice integration](https://github.com/lightningdevkit/rust-lightning/pull/4007)
  - [Add splice-out support](https://github.com/lightningdevkit/rust-lightning/pull/3979)
  - [Support scalar tweak to rotate holder funding key during splicing](https://github.com/lightningdevkit/rust-lightning/pull/3624)
- LND
  - [Implement Quiescence Protocol](https://github.com/lightningnetwork/lnd/pull/8270)

Network Graph
----
#### BOLT
- [Increase channel close delay to 72 blocks](https://github.com/lightning/bolts/pull/1270)
- [Path queries (feature 66/67)](https://github.com/lightning/bolts/pull/1259)

BOLT 11
----
#### BOLT
- [bolt11: clarify signature normalization requirements](https://github.com/lightning/bolts/pull/1284)
- [bolt 11: add test vector for p2tr fallback address](https://github.com/lightning/bolts/pull/1276)

BOLT 12
----
#### BOLT
- [BOLT 12](https://github.com/t-bast/bolts/blob/master/12-offer-encoding.md)
- [blip-0042: Bolt 12 Contacts](https://github.com/lightning/blips/pull/42)
- [BOLT 12: re-add recurrence support](https://github.com/lightning/bolts/pull/1240)
- [BOLT 12: Inconsistent bech32 padding validation across implementations](https://github.com/lightning/bolts/issues/1281)
- [Support async payments in BOLT 12](https://github.com/lightning/bolts/pull/1149)

#### Implementations
- Core Lightning
- Eclair
- LDK
- LND


Lightning Service Provider (LSP
----
#### BOLT
- [Extensible Liquidity Ads)](https://github.com/lightning/bolts/pull/1153)

#### Implementations
- Core Lightning
- Eclair
- LDK
- LND


Privacy
----
#### BOLT
- [Receiver-side random delays](https://github.com/lightning/bolts/pull/1263)

#### Implementations
- Core Lightning
- Eclair
- LDK
- LND

Dual-Funding
----
#### BOLT
- [BOLT 2](https://github.com/t-bast/bolts/blob/master/02-peer-protocol.md)
- [Dual funding reconnect commit_sig retransmission](https://github.com/lightning/bolts/pull/1289)
- [Allow non-initiator to RBF dual-funded channels](https://github.com/lightning/bolts/pull/1236)

#### Implementations
- Core Lightning
- Eclair
- LDK
- LND

Security
----
#### BOLT
- [Project Updates: Hybrid Channel Jamming Mitigation](https://github.com/lightning/bolts/issues/1218)
- [Security.md file added to BOLT](https://github.com/lightning/bolts/blob/master/SECURITY.md)

#### Implementations
- Core Lightning
- Eclair
- LDK
- LND



Other
----
#### BOLT
- [Attribution data (feature 36/37)](https://github.com/lightning/bolts/pull/1044)
- [Outgoing reputation and HTLC Accountability](https://github.com/lightning/bolts/pull/1280)
- [Assume option_channel_type](https://github.com/lightning/bolts/pull/1232)

#### Implementations
- Core Lightning
- Eclair
- LDK
- LND
