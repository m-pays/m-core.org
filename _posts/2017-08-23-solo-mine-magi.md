---
layout: post
title: "Solo Mine MAGI"
date: 2017-08-23, 23:36:00
comments: false
description: "Solo Mine MAGI"
keywords: ""
categories:
- Development
tags:
- Development
---

<div class="block_table text-font-14px">

<ol>

<li><p><a target="_blank" href="http://m-core.org/download/">Download wallet</a></p>
</li>

<li><p>Edit magi.conf to include the following lines:</p>
<pre>
<code class="html">
daemon=1
server=1
rpcport=8232
rpcallowip=127.0.0.1
rpcuser=randome_username
rpcpassword=randome_rpcpassword
</code>
</pre>
</li>

<li><p>Launch wallet or daemon and synchronize blockchain</p>
</li>

<li><p>Launch miner:</p>

<p>Linux or OS X:</p>
<pre>
<code class="html">
./minerd --url http://127.0.0.1:8232 --user rpcuser --pass rpcpass -t thread_numbers  -e cpu_efficiency
</code>
</pre>

<p>Or</p>

<p>Windows:</p>
<pre>
<code class="html">
minerd.exe --url http://127.0.0.1:8232 --user rpcuser --pass rpcpass -t thread_numbers  -e cpu_efficiency
</code>
</pre>
</li>

<li><p>Mining calculator</p>
<p class="text-font-mono">getminingbykhps 10</p>

<pre>
<code class="html">
{
    "hashrate (kh/s)" : 10.00000000,
    "difficulty" : 1.56666109,
    "difficulty(aver)" : 1.35112710,
    "blockvalue" : 5.23089843,
    "mining (XMG)" : {
        "1 hour" : 0.03245060,
        "1 day" : 0.77881439,
        "1 week" : 5.45170070
    }
}
</code>
</pre>
</li>

</ol>

</div>