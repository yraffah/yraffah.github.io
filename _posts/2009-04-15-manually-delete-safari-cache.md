---
layout: post
title: !binary |-
  2KXZhNi62KfYoSDYp9mE2YPYp9i0INmF2YYg2LPZgdin2LHZiiDZitiv2YjZ
  itin2Ys=
created: 1239787213
---
<p style="direction: rtl; text-align: right;">في بعض الأحيان يضطر المستخدم إلى إلغاء الكاش من المتصفح إما بسبب تغيير ما أو بسبب تعديل قام به مطور لموقع و لا يظهر التعديل بسبب الكاش أو لأي سبب آخر و يمكن إلغاء الكاش بسهولة من خلال قائمة Safari &gt; Empty Cache. لكن بعض المستخدمين يشتكون من مشكلة التجميد (التهنيق) في سفاري بسبب كِِِبر حجم ملف الكاش حيث أنه يتعذر استخدام سفاري بسبب هذه المشكلة و يقع المستخدم في ورطة عدم تمكنه من فتح سفاري لإلغاء الكاش! مما يؤدي إلى استمرار المشكلة التي بسببها إضطر المستخدم إلى إلغاء و حذف الكاش أصلاً.</p>
<p style="direction: rtl; text-align: right;">الحل يكمن في إلغاء الكاش يدويا لكن ذلك يتطلب التعامل مع سطر الأوامر و معرفة موقع الكاش في النظام. لا تقلقوا فقد أتيت لكم بخطوات سهلة و بسيطة و إن شاء الله تحل مشكلتكم...</p>
<p style="direction: rtl; text-align: right;">بعد فتح برنامج سطر الأوامر Terminal، قوموا بالذهاب إلى المسار الموجود أدناه علما أن "0cQ7xvfXFVyASfmi8Z+beU+++TI" سيكون مختلفا على جهازكم لأنه اسم عشوائي للمجلد. و لمعرفة اسم المجلد العشوائي هذا على جهازكم عليكم كتابة الأمر التالي (الحرف القبل الأخير ليس حرف o بل هو رقم صفر 0):</p><br />
<div dir="ltr"><code>
ls /private/var/folders/0c/
</code></div><br />
<p style="direction: rtl; text-align: right;">المسار المطلوب هو:</p><br />
<div dir="ltr"><code>
/private/var/folders/0c/0cQ7xvfXFVyASfmi8Z+beU+++TI/-Caches-/com.apple.Safari
</code></div> <br />
<p style="direction: rtl; text-align: right;">و للدخول إلى المسار هذا قوموا بكتابة السطر التالي (مع مراعاة تبديل <span style="font-family: -webkit-monospace;">0cQ7xvfXFVyASfmi8Z+beU+++TI <span style="font-family: GeezaPro;">حسب ما هو موجود في جهازكم):</span></span></p><br />
<div dir="ltr"><code>
cd /private/var/folders/0c/0cQ7xvfXFVyASfmi8Z+beU+++TI/-Caches-/com.apple.Safari
</code></div><br />
<p style="direction: rtl; text-align: right;">داخل هذا المجلد ستجدون مجلدات و ملفات لكن ما نحتاجه هو الملف Cache.db؛ قوموا بحذفه عن طريق كتابة السطر التالي:</p><br />
<div dir="ltr"><code>
rm Cache.db
</code></div><br />
<!--break-->
