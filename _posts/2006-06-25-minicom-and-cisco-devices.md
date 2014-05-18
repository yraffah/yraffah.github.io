---
layout: post
title: Minicom and CISCO Devices
created: 1151247502
---
<div dir="ltr">Minicom is giving me a pain in the @r$$.. I managed to install it from the FreeBSD ports comm/minicom and configured it in the following way:
<code>
lqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqk
x A - Serial Device : /dev/ugen0
x B - Lockfile Location : /var/spool/lock
x C - Callin Program :
x D - Callout Program :
x E - Bps/Par/Bits : 9600 8N1
x F - Hardware Flow Control : No
x G - Software Flow Control : No
x 
x Change which setting?
mqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqj
</code>
I'm using /dev/ugen0 because I'm connecting the rollover cable to the DB-9 BELKIN device that is connected over a USB connection to my FreeBSD machine. The moment I attach the device dmesg shows the following line:
<code>
ugen0: Belkin Components USB-232 Adapter, rev 1.10/2.08, addr 2
</code>
Which makes me assume that /dev/ugen0 is the correct device to use?!
However, I still can't connect, it still say it is <strong>offline</strong>! Any hints? 
</div>
