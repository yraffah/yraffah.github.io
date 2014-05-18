---
layout: post
title: !binary |-
  2YbYs9mK2KrZh9inIQ==
created: 1237643278
---
<p style="direction: rtl; text-align: right;">تصلني العديد من الأسئلة سواء من أصدقاء أو معارف و زملاء حول كيفية استعادة كلمة المرور للمستخدم في نظام الماك في حال نسيانها أو فقدانها و خصوصا لمن لا يستخدمون خاصية الدخول التلقائي للنظام (و هو أفضل في نظري). وللمعلومية هناك أكثر من طريقة منها ما <a href="#method1">يتطلب القرص</a> المرن و منها ما <a href="#method2">لا يتطلب ذلك</a> و إليكم تفاصيل و خطوات كل منها.</p>
<!--break-->
<p style="direction: rtl; text-align: right;"><a name="method1"></a><a name="method1"></a><strong><span style="text-decoration: underline;">الطريقة الأولى</span></strong></p>
<p style="direction: rtl; text-align: right;"><strong>مميزاتها:</strong></p>
<ul>
    <li>سهلة و بسيطة</li>
    <li>عبارة عن خطوتين</li>
</ul>
<p style="direction: rtl; text-align: right;"><strong>عيوبها:</strong></p>
<ul>
    <li>تتطلب الـ DVD الخاص بالنظام (يأتي مجانا مع الجهاز الجديد)</li>
</ul>
<p style="direction: rtl; text-align: right;"><strong>الطريقة:</strong></p>
<p style="direction: rtl; text-align: right;">يجب وضع القرص و إعادة تشغيل الجهاز و عند سماع صوت تشغيل الجهاز قوموا بالضغط على حرف C حتى ترون شكل الترس الدوار</p>
<ul>
    <li>اختاروا اللغة و من ثم اختاروا من القائمة Utilities &gt; Reset Password في تايقر أو Installer &gt; Reset Password في ليبارد و من ثم اختاروا القرص الصلب (Macintosh HD) و من ثم اسم المستخدم. لا تختاروا System Administrator (root) أبدا لأن هذا مستخدم آخر لا يهمك أبدا كـ مستخدم عادي للماك.</li>
    <li>أدخلوا كلمة المرور الجديدة مرتين و من ثم إضغطوا Save</li>
</ul>
<p style="direction: rtl; text-align: right;">بعد الإنتهاء من ذلك اختاروا Quit من القائمة مع إبقاء الضغط على زر الفأرة حتى يقوم النظام بإخراج القرص تلقائياً. و يمكنكم إعادة ضبط كلمة المرور للـ Keychain عبر برنامج Keychain Access حتى لا يقوم النظام بسؤالكم عن كلمة المرور مع كل تغيير أو أي نشاط يتطلب كلمة المرور و<a href="http://yousef.raffah.com/node/538">هذا الموضوع يشرح كيفية فعل ذلك بالتفاصيل</a>.</p>
<p style="direction: rtl; text-align: right;">&nbsp;</p>
<p style="direction: rtl; text-align: right;"><a name="method2"></a><strong><span style="text-decoration: underline;">الطريقة الثانية</span></strong></p>
<p style="direction: rtl; text-align: right;"><strong>مميزاتها:</strong></p>
<ul>
    <li>لا تتطلب قرص النظام</li>
</ul>
<p style="direction: rtl; text-align: right;"><strong>عيوبها:</strong></p>
<ul>
    <li>تتطلب التعامل مع سطر الأوامر و كتابة الأوامر بحذر</li>
    <li>يجب معرفة اسم المعرف أو الـ username القصير (الذي لا يحتوي على مسافات)<a name="username"></a></li>
</ul>
<p style="direction: rtl; text-align: right;"><strong>الطريقة:</strong></p>
<p style="direction: rtl; text-align: right;">يجب إعادة تشغيل النظام و الضغط على حرف S بعد سماع صوت تشغيل جهاز الماك حتى ترون شكل الترس الدوار.</p>
<p style="direction: rtl; text-align: right;">ستظهر أمامكم كلمات و جمل كثيرة لا يجب عليكم إلقاء لها أي بال لكن إنتظروا حتى ينتهي النظام من ذلك و ترون سطر الأوامر والشكل # لتقوموا بكتابة التالي</p>
<div dir="ltr"><code>
mount -uw /
</code><br />
<code>
passwd username
</code></div>
<p style="direction: rtl; text-align: right;">سيطلب النظام كلمة المرور الجديدة و من ثم يجب إدخالها مرة أخرى للتأكيد مع استبدالـ username باسم المُعرّف القصير الذي <a href="#username">ذكرناه سابقا</a> و لا تنسوا<a href="http://yousef.raffah.com/node/538"> إعادة ضبط كلمة المرور الخاصة بالـ Keychain و هنا ستجدون الطريقة بالتفصيل</a>.</p>
<p style="direction: rtl; text-align: right;">&nbsp;</p>
<p style="direction: rtl; text-align: right;">في حال عدم معرفتكم لاسم المُعَرّف القصير والذي ذكرته هنا، يمكنكم اتباع الخطوات التالية لإنشاء مستخدم جديد تماما مثل أول مرة قمتم بتشغيل الجهاز بعد شراءه (شَد بَلَد :) )</p>
<p style="direction: rtl; text-align: right;">&nbsp;</p>
<p style="direction: rtl; text-align: right;">يجب إعادة تشغيل النظام و الضغط على حرف S بعد سماع صوت تشغيل جهاز الماك حتى ترون شكل الترس الدوار.</p>
<p style="direction: rtl; text-align: right;">ستظهر أمامكم كلمات و جمل كثيرة لا يجب عليكم إلقاء لها أي بال لكن إنتظروا حتى ينتهي النظام من ذلك و ترون سطر الأوامر والشكل # لتقوموا بكتابة التالي</p>
<div dir="ltr"><code>
mount -uw /
</code><br />
<code>
rm /var/db/.AppleSetupDone
</code><br />
<code>
reboot
</code></div>
<p style="direction: rtl; text-align: right;">يمكنكم بعد ذلك إلغاء المستخدم القديم أو إعادة ضبط كلمة المرور التي نسيتموها.</p>
<p style="direction: rtl; text-align: right;">&nbsp;</p>
<p><span style="font-family: 'Lucida Grande'; font-size: 11px; line-height: 16px;"><br />
</span></p>
