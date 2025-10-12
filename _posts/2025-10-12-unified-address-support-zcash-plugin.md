---
title: Orchard / Unified Address Support in the Zcash Plugin for BTCPayServer
categories:
  - news
show_comments: false
---
We’re excited to share that, thanks to the **Zcash Community Grants** program, the Zcash plugin for **BTCPayServer** now supports **Orchard / Unified Address** enabling merchants to receive ZEC through the most advanced shielded pool, integrated directly into the plugin architecture.

There’s also a fix for **non-dollar custom rate rules**, allowing any currency rate to be derived from ZEC-BTC, and an entry has been added for **ZEC-EUR**.

#### Updating to Unified Address Support

If you’re already accepting ZEC using the plugin, switching to the new address type only requires updating your viewing key:

1. **Update the plugin’s Docker repository.**
   A new configuration and wallet file will be created automatically.

2. **Note the new files:**

   * Database file: `zec-wallet.db` (replaces `zec-wallet2.db`)
   * Configuration file: `config2.json` (inside the `zec_wallet` Docker volume)

3. **On first launch**, you’ll be prompted to enter your **Unified Full Viewing Key (UFVK)**.
   You may use the UFVK from the same wallet as before.

4. **Before updating**, check the **current Zcash block height** on [3xpl.com/zcash](https://3xpl.com/zcash) and note the number.
   You’ll need it when configuring the wallet — enter it as your **birth height** to scan only new Orchard transactions and skip older Sapling history.

Once complete, your server will begin receiving payments via **Unified Addresses**.

#### Getting Started

If you haven’t yet accepted ZEC through BTCPayServer, start with these setup guides:

* 📘 [**BTCPayServer Zcash Plugin Installation Guide**](https://github.com/btcpay-zcash/btcpayserver-zcash-plugin/blob/master/docs/installation.md) — official documentation.
* 🧭 [**ZecHub Guide**](https://zechub.wiki/guides/btcpayserver-zcash-plugin#content) — step-by-step instructions for configuring Zcash in BTCPayServer, with detailed explanations and examples.

#### Learn More About Unified Addresses and Orchard

To better understand how Unified Addresses and Orchard work, explore these resources from Electric Coin Co.:

* 🔍 [**Unified addresses in Zcash explained**](https://electriccoin.co/blog/unified-addresses-in-zcash-explained/) — an overview of the concept and its importance for Zcash evolution.
* ⚙️ [**ECC engineering year in review**](https://electriccoin.co/blog/ecc-engineering-year-in-review/) — insights into the transition to Orchard, Halo, and related protocol improvements.

#### Acknowledgments

Zcash Community Grants extends its gratitude to long-time community contributors — developers
[@hanh](https://forum.zcashcommunity.com/u/hanh/summary) and [@1337bytes](https://forum.zcashcommunity.com/u/1337bytes/summary) — for their invaluable work on maintaining and improving the Zcash plugin for BTCPayServer.

#### Get Involved

If you’re a merchant, developer, or enthusiast, test the integration, share feedback, and join the discussion on the [**Zcash Community Forum**](https://forum.zcashcommunity.com).
