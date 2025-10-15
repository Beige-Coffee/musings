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

## Dual-Funding
#### BOLT
- [BOLT 2](https://github.com/t-bast/bolts/blob/master/02-peer-protocol.md)
- [Dual funding reconnect commit_sig retransmission](https://github.com/lightning/bolts/pull/1289)
- [Allow non-initiator to RBF dual-funded channels](https://github.com/lightning/bolts/pull/1236)

#### Implementations
- Core Lightning
- Eclair
- LDK
- LND

## Splicing
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

 
## Lightning Service Provider (LSP
#### BOLT
- [Extensible Liquidity Ads)](https://github.com/lightning/bolts/pull/1153)
- [LSP Spec Transport Layer](https://github.com/lightning/blips/blob/master/blip-0050.md)
- [LSPS1: Channel Requests](https://github.com/lightning/blips/blob/master/blip-0051.md)
- [LSPS2: JIT Channel Negotiation](https://github.com/lightning/blips/blob/master/blip-0052.md)
- [LSPS5: Webhook Registration](https://github.com/lightning/blips/blob/master/blip-0055.md)

#### Implementations
- Core Lightning
- Eclair
- LDK
- LND


## Zero-Fee Commitments
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

## Simple Taproot Channels
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
- LND
  - [Release Notes 0.17.0](https://github.com/lightningnetwork/lnd/blob/master/docs/release-notes/release-notes-0.17.0.md)
 
## (Taproot) Gossip V1.75
#### BOLT
- [extension-bolt: taproot gossip (features 32/33)](https://github.com/lightning/bolts/pull/1059)
#### Implementations
- Core Lightning
- Eclair
- LDK
- LND
  - [[epic]: Gossip 1.75](https://github.com/lightningnetwork/lnd/issues/7961)
 

## Hybrid Channel Hamming
#### BOLT
- [Project Updates: Hybrid Channel Jamming Mitigation](https://github.com/lightning/bolts/issues/1218)

#### Implementations
- LND: [Add Experimental Endorsement Signalling](https://github.com/lightningnetwork/lnd/pull/8390)
- Eclair: [Add HTLC endorsement/confidence](https://github.com/ACINQ/eclair/pull/2884)

## Async Payments
#### BOLT
- [Support async payments in BOLT 12](https://github.com/lightning/bolts/pull/1149)
#### Implementations
- Core Lightning
- Eclair
  - [Add initial support for async payment trampoline relay](https://github.com/ACINQ/eclair/pull/2435)
  - [Add PeerReadyNotifier actor](https://github.com/ACINQ/eclair/pull/2464)
  - [Wake up wallet nodes before relaying messages or payments](https://github.com/ACINQ/eclair/pull/2865)
- LDK
  - [Support intercepting onion messages for offline peers](https://github.com/lightningdevkit/rust-lightning/pull/2973)
  - [Async payments message encoding and prefactor](https://github.com/lightningdevkit/rust-lightning/pull/3125)
  - [Support paying static invoices](https://github.com/lightningdevkit/rust-lightning/pull/3140)
  - [Async recipient-side of static invoice server](https://github.com/lightningdevkit/rust-lightning/pull/3618)
  - [Static invoice server](https://github.com/lightningdevkit/rust-lightning/pull/3628)
  - [Async payments followups](https://github.com/lightningdevkit/rust-lightning/issues/4135)
- LND

## Trampoline Routing
#### BOLT
- [Trampoline Routing (Feature 56/57)](https://github.com/lightning/bolts/pull/829)
- [Trampoline onion format (Feature 56/57)](https://github.com/lightning/bolts/pull/836)
#### Implementations
- Core Lightning
- Eclair
  - [Add trampoline onion support](https://github.com/ACINQ/eclair/pull/1209)
  - [Add initial support for async payment trampoline relay](https://github.com/ACINQ/eclair/pull/2435)
  - [Variable size for trampoline onion](https://github.com/ACINQ/eclair/pull/2810)
  - [Trampoline to blinded](https://github.com/ACINQ/eclair/pull/2811)
  - [Prepare attribution data for trampoline payments](https://github.com/ACINQ/eclair/pull/3109)
- LDK
  - [Trampoline](https://github.com/lightningdevkit/rust-lightning/issues/2299)
- LND
  - [routing+htlcswitch: implement the major variants of Trampoline routing](https://github.com/lightningnetwork/lnd/issues/6689)
- Electrum
  - [4.1.0 RELEASE-NOTES](https://github.com/spesmilo/electrum/blob/4.1.0/RELEASE-NOTES)


## BOLT 12
#### BOLT
- [BOLT 12](https://github.com/t-bast/bolts/blob/master/12-offer-encoding.md)
- [blip-0042: Bolt 12 Contacts](https://github.com/lightning/blips/pull/42)
- [BOLT 12: re-add recurrence support](https://github.com/lightning/bolts/pull/1240)
- [BOLT 12: Inconsistent bech32 padding validation across implementations](https://github.com/lightning/bolts/issues/1281)
- [Support async payments in BOLT 12](https://github.com/lightning/bolts/pull/1149)
#### Implementations
- Core Lightning
  - [Offers: Not just for breakfast anymore!](https://github.com/ElementsProject/lightning/pull/7833)
- Eclair
  - [Eclair v0.11.0](https://github.com/ACINQ/eclair/releases/tag/v0.11.0)
- LDK
  - [BOLT12 Offers Tracking Issue](https://github.com/lightningdevkit/rust-lightning/issues/1970)
  - [BOLT12 Has Arrived](https://lightningdevkit.org/blog/bolt12-has-arrived/)
- LND
  - LND does not support yet, but you run run [LNDK](https://github.com/lndk-org/lndk) alongside LND to support BOLT 12 

#### Implementations
- Core Lightning
- Eclair
- LDK
- LND
