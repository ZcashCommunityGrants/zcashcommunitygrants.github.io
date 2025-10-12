---
title: Orchard / Unified Address Support in the Zcash Plugin for BTCPayServer
categories:
  - news
show_comments: false
---
We’re excited to share that, thanks to the **Zcash Community Grants** program, the Zcash plugin for **BTCPayServer** now supports **Orchard / Unified Address** — enabling merchants to receive ZEC through the most advanced shielded pool, integrated directly into the plugin architecture.

There is also a fix for non-dollar custom rate rules, allowing any currency rate to be derived from ZEC-BTC, and an entry has been added for ZEC-EUR.

If you’re already accepting ZEC using the plugin, switching to the new address type only requires updating your viewing key:

After updating the plugin’s Docker repository, a new configuration and wallet file will be created — the database file `zec-wallet.db` will be used instead of `zec-wallet2.db`, together with the new configuration file, config2.json (located inside the `zec_wallet` Docker volume).

On the first launch, you’ll be prompted to enter your **Unified Full Viewing Key (UFVK)**. You may use the UFVK from the same wallet as before. Before updating, check the **current Zcash block height** on [3xpl.com/zcash](3xpl.com/zcash) and note the number — you’ll need it when configuring the wallet. Enter this value as your **birth height** to scan only new Orchard transactions and skip older Sapling history. Once complete, your server will start receiving payments via Unified Addresses.

_If you haven’t yet accepted ZEC through BTCPayServer, start with these setup guides:_

- [BTCPayServer Zcash Plugin Installation Guide](https://github.com/btcpay-zcash/btcpayserver-zcash-plugin/blob/master/docs/installation.md) — official documentation.
- [ZecHub](https://zechub.wiki/guides/btcpayserver-zcash-plugin#content) — Step-by-step guide for configuring Zcash in BTCPayServer — a more detailed walkthrough with explanations and examples.

To better understand how Unified Addresses and Orchard work, check out these articles from Electric Coin Co.:

- [Unified addresses in Zcash explained](https://electriccoin.co/blog/unified-addresses-in-zcash-explained/) — an overview of the concept and its importance for Zcash evolution.
- [ECC engineering year in review](https://electriccoin.co/blog/ecc-engineering-year-in-review/) — insights into the transition to Orchard, Halo, and related protocol improvements.

Zcash Community Grants extends its gratitude to long-time community contributors — developers [@hanh](https://forum.zcashcommunity.com/u/hanh/summary) and [@1337bytes](https://forum.zcashcommunity.com/u/1337bytes/summary) — for their invaluable work on maintaining and improving the Zcash plugin for BTCPayServer.

If you’re a merchant, developer, or enthusiast, test the integration, share feedback, and join the discussion on the Zcash Community Forum.

