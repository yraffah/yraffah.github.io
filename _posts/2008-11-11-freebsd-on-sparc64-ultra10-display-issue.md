---
layout: post
title: FreeBSD on SPARC64 Ultra10 Display Issue
created: 1226424692
---
<p style="text-align: center;direction: rtl;"><a href=""><img src="http://upload.wikimedia.org/wikipedia/commons/thumb/f/f0/13W3_Stecker.jpg/300px-13W3_Stecker.jpg" /></a></p>
<p style="direction: rtl; text-align: right;">لاحظت وجود جهاز صن ألترا١٠ ذو معالج سبارك٦٤ قديم في العمل غير مستخدم. فكرت في استغلاله و إعادة إحيائه بتثبيت نظام فري بي إس دي عليه و بالفعل قمت بذلك و تمت عملية تنصيب النظام من أبدع ما يكون :) إلا أنني واجهت مشكلة في عرض النظام على الشاشة و إليكم التفاصيل.</p>
<p style="direction: rtl; text-align: right;">الجهاز به كرت شاشة من نوع <a href="http://en.wikipedia.org/wiki/DB13W3">13W3</a> كما أن هناك كرت VGA موصول عليه من نوع (ATI Rage 3D). عند توصيل كرت الـ 13W3 فالشاشة تعمل بشكل طبيعي لكن عند توصيل الـ VGA لا يتم عرض أي شيء على الشاشة. قمت بعملية جوجلة سريعة و لم أصل لنتيجة فاستشرت خبراء النظام على القائمة البريدية الخاصة بنظام فري بي إس دي على معالجات سبارك٦٤ و جائني رد من أحد المشاركين يفيد بأن المشكلة تكمن في أن النظام و بشكل إفتراضي يقوم بعرض جميع مخرجاته على جهاز العرض الإفتراضي (13W3) لذلك لو أردت عرض مخرجات النظام على جهاز العرض الآخر فيتوجب علي إما فصل الكرت الأول (13W3) أو تحويل العرض إلي الكرت الثاني (VGA) من خلال الـ Open Boot Firmware. قررت إتخاذ القرار الثاني لأني لم أرد فتح الجهاز و خلافه وإختصارا للوقت كما أنني يمكن أن أستفيد من الشاشة الأخرى :).</p>
<p>إليكم تفاصيل الخطوات التي قمت بها؛</p>
<p>بداية أردت معرفة قيمة المتغير output-device وهو المطلوب تغييره</p>
<p style="direction: ltr; text-align: left;"><code>OK printenv output-device</code><br />
<code>screen</code></p>
<p>لمعرفة مسار جهاز العرض المطلوب في النظام:</p>
<p style="direction: ltr; text-align: left;"><code>OK show-devs</code></p>
<p>وجدت المسار كالتالي:</p>
<p style="direction: ltr; text-align: left;"><span style="font-family: Georgia;"><code>/pci@1f,0/pci@1,1/SUNW,m64B@2</code></span></p>
<p>بدلا من إعطاء المتغير output-device قيمة المسار بالكامل، قمت بعمل إختصار أو (اسم مستعار)</p>
<p style="direction: ltr; text-align: left;"><code>OK nvalias mach64</code> <span style="font-family: Georgia;"><code>/pci@1f,0/pci@1,1/SUNW,m64B@2</code></span><br />
<code>OK setenv output-device mach64</code><br />
<code>OK reset-all</code></p>
<p style="direction: rtl; text-align: right;"><span style="font-family: Georgia;">أثناء بحثي و جوجلتي وجدت مقالا رائعا أفادني كثيرا على الرابط:</span></p>
<p style="direction: rtl; text-align: right;"><span style="font-family: Georgia;"><a href="http://www.csn.ul.ie/~ivan/install_ubuntu_on_ultra10.html#OpenBoot%20Firmware">http://www.csn.ul.ie/~ivan/install_ubuntu_on_ultra10.html#OpenBoot%20Firmware</a><br />
</span></p>
<!--break-->
<p style="text-align: left;direction: ltr;">I had an extra Sun SPARC64 Ultra10 machine at work that was unplugged and doing nothing at all. I told myself, it would be cool to install FreeBSD on it and make it useful again :). Installation went through and the box is booting normally but I had a problem with the display.</p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia; min-height: 14px;">&nbsp;</p>
<p style="text-align: left;direction: ltr;">The machine I&rsquo;m playing with has the <a href="http://en.wikipedia.org/wiki/DB13W3">13W3</a> connector to hook up a monitor to as well as a normal on-board VGA card (ATI Rage 3D) which is called machfb0 frame-buffer. The problem when you connect both the cards to two monitors, the system defaults to run syscons on the primary AFB/FFB frame-buffer, which is by default the 13W3. Once this happens, you can&rsquo;t see anything on the machfb0 connected monitor except a white background! Even X won&rsquo;t run on that.</p>
<p style="text-align: left;direction: ltr;">I tried to google it but couldn&rsquo;t get a proper solution to the problem therefore I went to the FreeBSD-SPARC64 mailing list and asked. Not surprisingly got a grateful answer from someone named Marius Strobl detailing the problem and providing the proper solution.</p>
<p style="text-align: left;direction: ltr;">The solution was redirecting the primary frame-buffer to machfb0 in the Open Boot Firmware by changing the variable output-device to the full path of machfb0. Once I did that, everything worked fine, syscons was showing on the machfb0 connected monitor, X worked fine and I was even able to use a dual monitor setup :)</p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia; min-height: 14px;">&nbsp;</p>
<p style="text-align: left;direction: ltr;">Here is what I did;</p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia; min-height: 14px;">&nbsp;</p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia;"><code>OK printenv output-device</code></p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia;"><code>screen</code></p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia; min-height: 14px;">&nbsp;</p>
<p style="text-align: left;direction: ltr;">To know where is the device, I used:</p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia;"><code>OK show-devs</code></p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia; min-height: 14px;">&nbsp;</p>
<p style="text-align: left;direction: ltr;">Which listed my machfb0 at the following path:</p>
<p style="text-align: left;direction: ltr;"><code>/pci@1f,0/pci@1,1/SUNW,m64B@2</code></p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia; min-height: 14px;">&nbsp;</p>
<p style="text-align: left;direction: ltr;">Instead of typing the whole path, we can make an alias like this:</p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia;"><code>OK nvalias mach64 /pci@1f,0/pci@1,1/SUNW,m64B@2</code></p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia;"><code>OK setenv output-device mach64</code></p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia;"><code>OK reset-all</code></p>
<p style="text-align: left;margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; font: 12px Georgia; min-height: 14px;">&nbsp;</p>
<p style="text-align: left;direction: ltr;">During my google search, I found a very helpful resource at <a href="http://www.csn.ul.ie/~ivan/install_ubuntu_on_ultra10.html#OpenBoot%20Firmware">http://www.csn.ul.ie/~ivan/install_ubuntu_on_ultra10.html#OpenBoot%20Firmware</a></p>
