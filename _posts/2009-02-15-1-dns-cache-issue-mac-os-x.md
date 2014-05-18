---
layout: post
title: !binary |-
  2KXYudin2K/YqSDYttio2Lcg2KfZhNmA2YPYp9i0INmB2Yog2KfZhNmARE5T
  INmE2YbYuNin2YUgTWFjIE9TIFg=
created: 1234687802
---
<p><span style="font-family: Verdana; ">&nbsp;في بعض الأحيان يضطر المرء إلى إعادة ضبط أو إلغاء الكاش الخاص بالـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span> لتفادي بعض من معوقات أو مشاكل الـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span> و خصوصا التي تتعلق بالكاش. مثال على ذلك هو حينما تعمل على نقل خادم من <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">IP</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Address</span> إلى <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">IP</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Address</span> آخر فـ عادة سيكون الـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">IP</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Address</span> القديم مخزنا في الكاش في جهازك حتى وقت إنتهاء صلاحية المعلومات (حسب إعدادات الـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS) </span>و<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>هو<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>ما<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>يسمى<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>الـ<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> Cache Expiry.</span></span></p>
<span style="font-family: Verdana; ">
<p>و<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>لإعادة<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>ضبط<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>الكاش<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>و<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>مسح<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>محتوياته القديمة في الـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Mac</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">OS</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">X</span> هناك أمران، أحدهما لنظام ليبارد والآخر لنظام تايقر. تتم كتابة أي من الأمرين، حسب نسخة النظام لديك، في سطر الأوامر والمعروف في الـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Mac OS X </span>باسم<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> Terminal.app.</span></p>
</span>
<!--break-->
<h3><span style="font-family: Verdana; ">بداية ما هي فائدة الـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Cache</span>؟<br />
</span></h3>
<p><span style="font-family: Verdana; ">عندما يقوم جهازك بطلب عنوان <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">IP</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Address</span> لموقع معين كـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; "><a href="http://Yousef.Raffah.com">Yousef</a></span><a href="http://Yousef.Raffah.com">.</a><span style="font: normal normal normal 12px/normal 'Lucida Grande'; "><a href="http://Yousef.Raffah.com">Raffah</a></span><a href="http://Yousef.Raffah.com">.</a><span style="font: normal normal normal 12px/normal 'Lucida Grande'; "><a href="http://Yousef.Raffah.com">com</a></span> مثلا فإن عميل الـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span> في جهازك (<span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Client</span>) يطلب من خادم الـ<span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span> المعرف في إعدادات النظام أو الشبكة لديك و سيقوم الأخير بالرد عليه. لكن لو قمت بطلب الموقع <span style="font: normal normal normal 12px/normal 'Lucida Grande'; "><a href="http://Yousef.Raffah.com">Yousef</a><a href="http://Yousef.Raffah.com">&nbsp;</a></span><span style="font: normal normal normal 12px/normal 'Lucida Grande'; "><a href="http://Yousef.Raffah.com">Raffah</a></span><a href="http://Yousef.Raffah.com">.</a><span style="font: normal normal normal 12px/normal 'Lucida Grande'; "><a href="http://Yousef.Raffah.com">com</a></span> مرة أخرى بعد ذلك فإن عميل الـ<span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span> لديك لن يطلب العنوان من خادم الـ<span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span> بل سيقوم بتوفيره لك من الـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS Cache </span>و<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>ذلك<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>لأنه قام بتخزين القيمة مسبقا وبالتالي إلى سرعة<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>توفر<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>المعلومة<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>وهذا بدوره سيساهم في سرعة تصفح المواقع والوصول للخوادم. لكن ماذا سيحصل لو كان عنوان الـ<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> IP Address </span>الذي قدمه الخادم لك (من أول مرة) ليس صحيحا!! بذلك ستقوم في كل مرة تطلب نفس الخادم بالوصول إلى نفس النتيجة الخاطئة.</span></p>
<p><span style="font-family: Verdana; ">الحل هو إما عملية مسح القيمة من الكاش و هي ما يمكن تسميته إصطلاحا إعادة ضبط الكاش أو <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Flushing</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">the</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">cache </span>لحل<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>المشكلة<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>سريعا<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>أو<span style="font: normal normal normal 12px/normal 'Lucida Grande'; "> </span>الإنتظار لمدة ٢٤ ساعة أو أكثر (حسب إعدادات الـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span>)!</span><span style="font-family: Verdana; "><br />
</span></p>
<p><span style="font-family: Verdana; ">إعادة ضبط و مسح الكاش الخاص بالـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span> في <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Mac OS x 1.5 </span>ليبارد</span><span style="font-family: Verdana; "><br />
</span></p>
<p>بعد تشغيل برنامج الـ <span style="font: normal normal normal 12px/normal 'Verdana'; ">Terminal</span> قم بكتابة الأمر التالي:</p>
<div dir="ltr"><code>
dscacheutil -flushcache
</code></div>
<span style="font-family: Verdana; ">
<p>بهذا نكون قد ألغينا و مسحنا الكاش الخاص بالـ DNS</p>
</span>
<p><span style="font-family: Verdana; ">إعادة ضبط و مسح الكاش الخاص بالـ <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">DNS</span> في <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">Mac</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">OS</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">X</span> <span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">10</span>.<span style="font: normal normal normal 12px/normal 'Lucida Grande'; ">4</span> تايقر
<trong>
</trong>
</span></p>
<p><span style="font-family: Verdana; ">بعد تشغيل برنامج الـ <span style="font: normal normal normal 12px/normal 'Verdana'; ">Terminal</span> قم بكتابة الأمر التالي:</span></p>
<div dir="ltr"><code>
lookupd -flushcache
</code></div>
<br />
<br />
<br />
<h4><span style="font: 12.0px Geeza Pro">المصادر</span>:: Sources</h4>
<div dir="ltr">
<ul>
    <li><a href="http://osxdaily.com/2008/03/21/how-to-flush-your-dns-cache-in-mac-os-x/">http://osxdaily.com/2008/03/21/how-to-flush-your-dns-cache-in-mac-os-x/</a></li>
    <li><a href="http://www.macosxhints.com/article.php?story=20071027100807321">http://www.macosxhints.com/article.php?story=20071027100807321</a></li>
    <li><a href="http://www.tech-faq.com/flush-dns.shtml">http://www.tech-faq.com/flush-dns.shtml</a></li>
</ul>
</div>
<br />
<br />
