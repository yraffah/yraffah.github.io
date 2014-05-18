---
layout: post
title: !binary |-
  2YPZitmB2YrYqSDYqti02LrZitmEIE5URlPZgtix2KfYodipINmIINmD2KrY
  p9io2Kkg2LnZhNmJINin2YTZhdin2YM=
created: 1187010906
---
<p>ما أحلى الـ Open Source</p>
<h2>تحديث مهم:</h2>
<p><h4>لقد تم كتابة نسخة جديدة من الموضوع بطريقة أسهل بكثير على هذا الرابط <a href="http://yousef.raffah.com/node/518">"طريقة جديدة و محدثة للكتابة على الـ NTFS في الماك"</a></h4></p>
<p>لقد تمكنت من تشغيل&nbsp; NTFSقراءة و كتابة على الماك و ذلك باستخدام برامج Open Source حرة و مفتوحة المصدر، و هذا الكلام يوجه لمن لا يؤمن بقوة فلسلفة المصادر المفتوحة. نعود لموضوعنا الأساسي، يجب تثبيت حزمتين لإنهاء العملية والخطوات سهلة و سأحاول تبسيطها هنا.</p>
<p>أولا تثبيت المتطلبات و هي حزمة MacFUSE و يمكن تحميلها&nbsp; و <a href="http://macfuse.googlecode.com/files/MacFUSE-Core-0.4.0.dmg">هذا رابط مباشر</a> <a href="http://code.google.com/p/macfuse/downloads/list">من هنا</a>. ثم نقوم بعملية التثبيت و هي كتثبيت أي برنامج في الماك.</p>
<p>بعد ذلك نقوم بتثبيت الحزمة التي تمكننا من تشغيل الدرايفر الخاص والذي يمكننا من قراءة و كتابة نظام الملفات NTFSوالذي يسمى NTFS-3G و يمكن تحميله <a href="http://homepage.mac.com/danielj7/NTFS-3G.pkg.tar.bz2">من هنا</a>. ثم نقوم بعملية التثبيت و هي كتثبيت أي برنامج في الماك.</p>
<p>الخطوة الأخيرة، يجب التأكد من عدم وجود أي ربط (mount) لبارتشن من نوع NTFS و ذلك بكتابة الأمر التالي في التيرمنال</p>
<p><code>diskutil list | grep Windows_NTFS</code></p>
<p>إذا كان هناك بارتشن مربوط (mounted) قوموا بعمل eject له و إن لم يكن هناك أي إرتباط قوموا بالخطوة التالية في التيرمنال ولكن قبل ذلك تأكدوا من مسار البارتشن المراد ربطه، يمكنكم معرفة المسار باستخدام الأمر السابق diskutil على النحو التالي:</p>
<div dir="ltr"><code>
diskutil list
</code></div><br />
<div dir="ltr"><code>/dev/disk0
   #:                       TYPE NAME                    SIZE       IDENTIFIER
   0:      GUID_partition_scheme                        *149.1 Gi   disk0
   1:                        EFI                         200.0 Mi   disk0s1
   2:                  Apple_HFS Macintosh HD            148.7 Gi   disk0s2
/dev/disk1
   #:                       TYPE NAME                    SIZE       IDENTIFIER
   0:     FDisk_partition_scheme                        *298.1 Gi   disk1
   1:                  Apple_HFS iBeastie                198.5 Gi   disk1s1
   2:               Windows_NTFS BeaSDe                  99.6 Gi    disk1s2
</code></div>
<p>هنا نرى أن البارتشن الذي يجب ربطه هو disk1s2 و سنقوم بذلك الآن</p>
<div dir="ltr"><code>
mkdir /Volumes/ntfs
</code></div>
<p>هذا الأمر السابق لا نحتاجه سوى أول مرة، بعد ذلك لن نستخدمه</p>
<p>الأمر التالي يجب كتابته كل مرة نريد ربط أي بارتشن بنظام الملفات NTFS و يمكن استبدال BeaSDe بأي اسم تريدونه أن يظهر على سطح المكتب</p>
<div dir="ltr">
<code>
ntfs-3g /dev/disk1s2 /Volumes/ntfs -ovolname="BeaSDe"
</code></div>
<p>&nbsp;</p>
<p>المصدر:</p>
<p><a href="http://www.daniel-johnson.org/">http://www.daniel-johnson.org/</a></p>
<p><a href="http://www.ntfs-3g.org/">www.ntfs-3g.org/</a></p>
