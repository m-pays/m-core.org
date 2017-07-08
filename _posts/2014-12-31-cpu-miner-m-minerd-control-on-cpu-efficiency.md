---
layout: post
title: "CPU miner - m-minerd control on CPU efficiency"
date: 2014-12-31, 04:30:55
comments: false
description: "CPU miner - m-minerd control on CPU efficiency"
keywords: ""
categories:
- Mining
tags:
- Mining
---

<div class="block_table text-font-14px">

<p>We introduce a CPU miner (<a target="_blank" href="https://github.com/magi-project/m-cpuminer-v2">m-minerd</a>) with the capability of adjusting CPU efficiency, targeting at improved response to MAGI's PoW operation. In the generic PoW, mining with reduced CPU efficiency leads to reduced rewards since the other miners always pursue higher hashrates.</p> 

<p>In MAGI's PoW implementation, pursuing high hashrate is recommended only at some occasions (passive mining phase), and will be greatly frustrated once the total network hashrate is over the limit (agressive mining phase). At the time when network hashrate reaches a limit, reduced hashrate will actually benefit to save energy cost since the excess hashrate is not adding up to obtain rewards.</p>


<p>Basic command to run m-minerd: </p>

<p class="text-font-mono">minerd -o stratum+tcp://pool_url:pool_port -u pool_user.worker -p password -t thread_numbers -e cpu_efficiency</p>


<p>where the option "-e cpu_efficiency" is to set how much CPU usage is utilized; cpu_efficiency has to be between 1 - 100. </p>

<br>
<p><u>Example:</u></p>

<p>Notice the variation of CPU temperature with the value of -e flag. </p>

<p>
-e 75: <img src="/assets/img/blog/2014-12-31-m-minerd/cpu-75.png"><br>

-e 50: <img src="/assets/img/blog/2014-12-31-m-minerd/cpu-50.png"><br>

-e 25: <img src="/assets/img/blog/2014-12-31-m-minerd/cpu-25.png"><br>

-e 1: <img src="/assets/img/blog/2014-12-31-m-minerd/cpu-1.png">
</p>

<br>

<p><u>Download:</u></p>
<p>
<a href="/download#cpu-miner-source" class="black-color">source code</a>, <a href="/download#cpu-m-minerd" class="black-color">command-line binaries: m-minerd</a> and <a href="/download#cpu-m-cpuminer-qt" class="black-color">GUI binaries: m-cpuminer-qt</a>
</p>

<br>

<p><u>CPU efficiency adjusted using external programs:</u></p>

<p>Miners by <a href="/download#cpu-miner-Spexx" class="black-color">Spexx</a> and <a href="/download#cpu-miner-NeedIfFindIt" class="black-color">NeedIfFindIt</a>.
</p>

</div>