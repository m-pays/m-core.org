---
layout: post
title: "MAGI Core version 1.4.3 released"
date: 2017-08-24, 22:00:00
comments: false
description: "MAGI Core version 1.4.3 released"
keywords: ""
categories:
- Development
tags:
- Development
---

<div class="block_table text-font-14px">

<br>
<div class="page-sub-title">
Changelog: 
</div>

<p>This release is a temporary fix to the current blockchain issue in MAGI; this is done by taking 104.128.225.215 as a trust node. Following setting in magi.conf is highly recommended. Refer to <a href="http://m-core.org/blog">http://m-core.org/blog</a> for news and final fix to the issue.
</p>

<br>
<p>
v1.4.3<br>
=============<br>
</p>

<p>
<a href="http://coinmagi.org/bin/m-wallet-1.4.3/">http://coinmagi.org/bin/m-wallet-1.4.3/</a><br>
Source code: <a href="https://github.com/magi-project/magi/">https://github.com/magi-project/magi/</a><br>

Windows (ZIP): <a href="http://coinmagi.org/bin/m-wallet-1.4.3/m-wallet-1.4.3-win.zip">http://coinmagi.org/bin/m-wallet-1.4.3/m-wallet-1.4.3-win.zip</a><br>
Linux:<a href="http://coinmagi.org/bin/m-wallet-1.4.3/m-wallet-1.4.3-linux.tar.gz">http://coinmagi.org/bin/m-wallet-1.4.3/m-wallet-1.4.3-linux.tar.gz</a><br>
Mac OS X: <a href="http://coinmagi.org/bin/m-wallet-1.4.3/m-wallet-1.4.3-osx.dmg">http://coinmagi.org/bin/m-wallet-1.4.3/m-wallet-1.4.3-osx.dmg</a><br>

Block chain (#1451225): <a href="http://coinmagi.org/bin/block-chain/">http://coinmagi.org/bin/block-chain/</a><br>
Release notes: <a href="http://coinmagi.org/bin/release-notes.md">http://coinmagi.org/bin/release-notes.md</a>
</p>

<br>
<div class="page-sub-title">
Notes: 
</div>

<ul>
<li>PoW Block reward: 30% of normal value for temporary and back to normal after the fix is fully done;</li>
<li>PoS rewards: 20% more also temporarily and back to normal after the fix is fully done.</li>
</ul>

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

<br>
<div class="page-sub-title">
Solo mining:  
</div>
<br>

<a href="http://m-core.org/solo-mine-magi/">http://m-core.org/solo-mine-magi/</a>

</div>