---
layout: post
title: "MAGI Core version 1.4.4.1 released"
date: 2017-09-14, 23:56:00
comments: false
description: "MAGI Core version 1.4.4.1 released"
keywords: ""
categories:
- Development
tags:
- Development
---

<div class="block_table text-font-14px">

<br>
<p>This release solves the recent blockchain forking issue.</p>

<div class="page-sub-title">
Changelog
</div>

<p>- Synchronizing checkpoint & master server introduced; this is to remove constantly checking on the misbehaving and IP banning, along with the error "block with too little proof-of-stake or proof-of-work". The checkpoint master server and keys remain to be used from now on; they are likely to be removed in the future;</p>

<p>- Implemented a block generation rule: PoW / PoS blocks are mined / minted by following a pattern: 1) at least two PoS blocks minted between two consecutive PoW blocks, or PoW blocks generated every 10 minutes; 2) at least one PoW block is found in five consecutive PoS blocks, or PoS blocks generated every 3 minutes;</p>

<p>- Difficulty adjustment will be changed to four-block exponential moving average. When there is violation in aforementioned PoW / PoS generation rule, the difficulty remains unchanged. </p>

<p>The following hard forks are scheduled to implement the changes:</p>

- block 1481500: PoW / PoS block generation rule, and also exit point of the maintenance mode;<br>
- block 1482000: difficulty adjustment algorithm switch.<br>

<div class="page-sub-title">
Nodes 
</div>

<p>
- 104.128.225.215<br>
- 45.35.251.73<br>
</p>

<p>
v1.4.4.1<br>
=============<br>
</p>

<p>
<a href="http://coinmagi.org/bin/m-wallet-1.4.4.1/">http://coinmagi.org/bin/m-wallet-1.4.4.1/</a><br>
Source code: <a href="https://github.com/magi-project/magi/">https://github.com/magi-project/magi/</a><br>

Windows (ZIP): <a href="http://coinmagi.org/bin/m-wallet-1.4.4.1/m-wallet-1.4.4.1-win.zip">http://coinmagi.org/bin/m-wallet-1.4.4.1/m-wallet-1.4.4.1-win.zip</a><br>
Linux:<a href="http://coinmagi.org/bin/m-wallet-1.4.4.1/m-wallet-1.4.4.1-linux.tar.gz">http://coinmagi.org/bin/m-wallet-1.4.4.1/m-wallet-1.4.4.1-linux.tar.gz</a><br>
Mac OS X: <a href="http://coinmagi.org/bin/m-wallet-1.4.4.1/m-wallet-1.4.4.1-osx.dmg">http://coinmagi.org/bin/m-wallet-1.4.4.1/m-wallet-1.4.4.1-osx.dmg</a><br>

Block chain: <a target="_blank" href="http://coinmagi.org/bin/block-chain/">http://coinmagi.org/bin/block-chain/</a><br>
Release notes: <a target="_blank" href="http://coinmagi.org/bin/release-notes.md">http://coinmagi.org/bin/release-notes.md</a>
</p>

<div class="page-sub-title">
Setup
</div>

<p>
- Windows: double click to install, or unpack the files and run the wallet directly;<br>
- Mac OS: unpack the files and copy to the Application folder, and then run the wallet directly;<br>
- Linux: unpack the files and run the wallet directly. <br>
</p>

<p>For a fast startup:</p>

1) Download latest block-chain data from here: <a target="_blank" href="http://coinmagi.org/bin/block-chain/">http://coinmagi.org/bin/block-chain/</a>;<br>
2) Unzip the file and copy the folders under "m-block-chain" into the .magi (unix-like system) or Magi (OS X or Windows) folder;<br>
3) Launch the new wallet. <br>

<br>

<p>If you were using version prior to v1.4.4.0, the old block chain data must be deleted before launching the new wallet:</p>

1) Backup wallet.dat;<br>
2) Delete all of the contents under the .magi (unix-like system) or Magi (OS X or Windows) folder, except for wallet.dat and magi.conf;<br>

<div class="page-sub-title">
Info
</div>
<p>
- Website: <a target="_blank" href="http://www.m-core.org">http://www.m-core.org</a> <br>
- Bitcointalk thread: <a target="_blank" href="https://bitcointalk.org/index.php?topic=735170.0">https://bitcointalk.org/index.php?topic=735170.0</a> <br>
- Forum: <a target="_blank" href="http://www.m-talk.org/">http://www.m-talk.org/</a> <br>
- Slack: <a target="_blank" href="http://slack.m-core.org">http://slack.m-core.org</a> <br>
- Freenode IRC: <a target="_blank" href="https://kiwiirc.com/client/irc.freenode.net/#magi">#magi</a> <br>
- Twitter Marketing: <a target="_blank" href="https://twitter.com/Coin_Magi_XMG">https://twitter.com/Coin_Magi_XMG</a> <br>
- Twitter Dev: <a target="_blank" href="https://twitter.com/CoinMagi">https://twitter.com/CoinMagi</a> <br>
- Facebook: <a target="_blank" href="http://www.facebook.com/CoinMagi">http://www.facebook.com/CoinMagi</a> <br>
</p>

</div>
