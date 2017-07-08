---
layout: post
title: "MAGI - New Added API Calls"
date: 2014-12-31, 04:30:55
comments: false
description: "MAGI - New Added API Calls"
keywords: ""
categories:
- Development
tags:
- Development
---

<div class="block_table text-font-14px">
<p>Several added API calls for MAGI: getnetstakeweight, getmininginfo, getnewblockvaluebynumber, and getminingbykhps.</p>

<ol>

<li><p>Network stake weight</p>
<p class="text-font-mono">getnetstakeweight</p>
</li>

<li><p>Mining info</p>
<p class="text-font-mono">getmininginfo</p>

<pre>
<code class="html">
{
    "Expected PoS (hours)" : 3
}
</code>
</pre>
</li>

<li><p>Block reward</p>
<p class="text-font-mono">getnewblockvaluebynumber 122478</p>

<pre>
<code class="html">
{
    "flags" : "proof-of-work",
    "difficulty" : 1.62299710,
    "difficulty-V2" : 1.54876817,
    "blockvalue" : 5.36191184,
}
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