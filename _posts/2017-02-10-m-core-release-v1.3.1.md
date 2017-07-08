---
layout: post
title: "MAGI Core version 1.3.1 released"
date: 2017-02-10, 03:35:14
comments: false
description: "MAGI Core version 1.3.1 released"
keywords: ""
categories:
- Development
tags:
- Development
---

<div class="block_table text-font-14px">

<div class="page-sub-title">
Multiple Platforms: 
</div>

<p>Starting from v1.3.1, we provide official support of building packages for FreeBSD; both Qt wallet and daemon are available. Supports to other platforms may also occur in future release.</p>

<br>
<div class="page-sub-title">
Changelog: 
</div>

<br>
<p>
v1.3.1<br>
=============<br>
This is a major release designed to improve the overall performance of the wallet. Upgrading to this version is strongly recommended. All parties upgrading from versions prior to v1.3.0 should resynchronize the complete block chain from the beginning. 
</p>

<p>
A copy of block chain available: http://coinmagi.org/bin/block-chain/
</p>

<p>
- Support of building Qt wallet and daemon on FreeBSD;<br>
- Added "Mint" menu on the Qt wallet;<br>
- Added "About" menu on the Qt wallet;<br>
- Fixed price update for all of OS including Windows; <br>
- Corrected the total amount on the transaction page; <br>
- Overall improvement of the Qt wallet appearance;<br>
- Removed pre-release message from the status bar; <br>
- Redesigned the icon set; new logo available here: http://coinmagi.org/files/logo/v1; previous version: http://coinmagi.org/files/logo/v2;
</p>

<p>
(January 29, 2017)
</p>

<p>
This release also contains the prior changes associated with v1.3.0rc1 which wasn't made publicly. 
</p>

<p>
v1.3.0rc1<br>
=============<br>
- Changed database for storing transaction and block indices from Berkeley DB to LevelDB; <br>
- Enabled block hash storing in storage and loaded directly from disk;<br>
- Fixed "Checkpoint is too old" warning;<br>
- PoS stake splitting and combining features, which can be set by stakesplitthreshold=VALUE and stakecombinethreshold VALUE in magi.conf, or by RPC commands: setstakesplitthreshold and setstakecombinethreshold; RPC commands getstakesplitthreshold and getstakecombinethreshold to show their current values;<br>
- Added price information on Qt overviewpage;<br>
- Qt wallet logo change and GUI improvements;<br>
- Merge pull request of adding total balance in "Transactions" page by lightsplasher;<br>
- Merge pull request of version check updates by feldenthorne; fixed automatic version check including test/rc versions.
</p>

<p>
(June 22, 2016)
</p>

<br>
<div class="page-sub-title">
Qt-Wallet and Daemon: 
</div>

<p>
<a href="http://coinmagi.org/bin/m-wallet-1.3.1/">http://coinmagi.org/bin/m-wallet-1.3.1/</a><br>
Source code: <a href="https://github.com/magi-project/magi/">https://github.com/magi-project/magi/</a><br>

Windows Installer (x32/x64): <a href="http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-win-setup.exe">http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-win-setup.exe</a><br>
Windows (x32): <a href="http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-win32.zip">http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-win32.zip</a><br>
Windows (x64): <a href="http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-win64.zip">http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-win64.zip</a><br>

Linux:<a href="http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-linux.tar.gz">http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-linux.tar.gz</a><br>
Mac OS X: <a href="http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-osx.dmg">http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-osx.dmg</a><br>
FreeBSD: <a href="http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-freebsd.tar.g">http://coinmagi.org/bin/m-wallet-1.3.1/m-wallet-1.3.1-freebsd.tar.gz</a><br>

Block chain: <a href="http://coinmagi.org/bin/block-chain/">http://coinmagi.org/bin/block-chain/</a><br>
Release notes: <a href="http://coinmagi.org/bin/release-notes.md">http://coinmagi.org/bin/release-notes.md</a>
</p>

<br>
<div class="page-sub-title">
Notes: 
</div>

<ul>
<li>Since v1.3.1 migrates to leveldb for block index storing, for upgrading from a version before v1.3 should reset the local block-chain;</li>
<li>For users on Windows, we provide a convenient way to use an installer for upgrading wallet and migrating to the latest block chain; this is strongly recommended; </li>
<li>Additional note to the stake splitting & combing for information; https://github.com/magi-project/magi/blob/1.3.0rc/src/wallet.cpp#L1595</li>
</ul>

<br>
<p class="text-font-mono">
                // The original design prevents stakes having the same parent transaction from combining <br>
                // which somehow reads as encouraging splitting (improve security); <br>
                // This mechanism is to be disabled in Magi since combining won't cause security concern <br>

                /* Splitting is only enforced at wallet, not by PoS protocol as well as consensus over network. <br>
                 * Original PPCoin design encourages splitting as per "Lower coinstake combine threshold to <br>
                 * improve security", which can be understood by the fact that in general PoS, with a large <br>
                 * number of coins in stake comes greater chance of (PoS) mining blocks. This is not going to <br>
                 * happen in Magi. Also, hardening nStakeCombineThreshold is impractical since an advanced user <br>
                 * can easilly make a change to that and rebuild a wallet. The change to nStakeCombineThreshold <br>
                 * should be available externally, e.g., RPC command, magi.conf configuration file. <br>
                 ** Magi, for optimum staking, nStakeCombineThreshold should be used in combination with <br>nStakeSplitThreshold.*/
</p>

<p>
nStakeCombineThreshold along with nStakeSplitThreshold should be utilized for best results. The optimum threshold is neither a random number nor as large as possible; it's in accordance with the magi's PoS (mPoS) protocol.  
</p>

<br>
<div class="page-sub-title">
Upgrade: 
</div>
<br>

<p>
- In general: <br>
1) Backup wallet.dat;<br>
2) Delete everything under the Magi or .magi folder except wallet.dat;<br>
3) Download block chain from here http://coinmagi.org/bin/block-chain/ and unzip the file;<br>
4) Put all of the contents under the folder m-blockchain into Magi or .magi;<br>
5) Launch the new wallet. <br>
</p>

<p>
- Windows: <br>
1) Backup wallet.dat;<br>
2) Launch the installer;<br>
3) Choose the option you want to migrate the block-chain; the installer will always move the original Magi folder to something like Magi-BACKUP-*;<br>
4) Follow on-screen prompts to install.<br>
</p>


<p>
<img src="/assets/img/blog/2017-02-10-m-core-release-v1.3.1/m-wallet-windows-installer_20170210.png"><br>
(One can also use the installer to update/switch block-chain data. We will update the block-chain from time to time)
</p>

<p>
We need have all of the services, mining pools and exchanges to switch to v1.3.1. Also, updating logo to v2 (<a href="http://coinmagi.org/files/logo/v2">http://coinmagi.org/files/logo/v2</a>) is recommended. 
</p>

</div>