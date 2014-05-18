---
layout: post
title: !binary |-
  2LnZhdmE2YrYqSDYpdi52K/Yp9ivINiz2YrYsdmB2LEgUkFOQ0lEINmE2YXY
  sdin2YLYqNipINin2YTYqti62YrZitix2KfYqiDZgdmKINij2KzZh9iy2Kkg
  2LPZitiz2YPZiA==
created: 1186308154
---
<p><br />
رانسيد <a href="http://www.shrubbery.net/rancid/">RANCID</a> هي اختصار لـ Really Awesome New Cisco ConfIg Differ<br />
و عند إعداد خادم رانسيد فإنك ستحصل على رسالة بالبريد الإلكتروني عن أي تعديل يحصل لأي من راوترات أو سويتشات أو فايرولات سيسكو و سيكون مضمون الرسالة موضحا لما كان عليه ملف إعدادات سيسكو السابق و ما هو التعديل الذي طرأ عليه. أضف إلى أنه يراقب أي تعديل في السوفتواير أو الهاردوير أو حتى رقم السيريال و يستخدم في ذلك نظام <a href="http://en.wikipedia.org/wiki/Concurrent_Versions_System">CVS</a> أو <a href="http://en.wikipedia.org/wiki/Subversion_%28software%29">SVN</a> للنسخ المتعدد Versioning.<br />
<br />
حقيقة لم أعرف أن هناك برنامج رائع بهذا الشكل و لم أسمع عنه من قبل لكني وجدته بالصدفة أثناء بحثي في الإنترنت بالأمس و قمت بتثبيته على أحد خوادم FreeBSD في العمل و كانت النتائج أكثر من رائعة، مذهلة في الحقيقة.<br />
<br />
<strong><font color="#339966">مالفائدة من برنامج كهذا؟</font></strong><br />
أولا في بيئات العمل الكبيرة يجب أن يكون هناك إعدادات قياسية لأي من الأجهزة، و بالأخص في أجهزة الشبكة مثل أجهزة سيسكو و هو ما يسمى بالـ Standardization حتى تسهل عملية إدارة عدد كبير من الأجهزة.<br />
أضف إلى ذلك أن وجود أكثر من مسؤول عن الشبكة (Network Admin) قد يصعب العملية و ربما يصعب تتبع الأخطاء في حال تغيير قيم معينة و ما إلى ذلك. لذى، وجود نظام نسخ متعدد Versioning System و ربطه بملف إعدادات سيسكو هو الحل الأمثل لهذا كما أنه يقوم بعمل نسخة احتياطية لملف إعدادات سيسكو، و صدقوني هذا أمر في غاية الأهمية لأنه قد يأتي يوم تتمنون وجود نسخة احتياطية للملف لتتفاجئون بعدم وجوده!!<br />
<br />
<strong><font color="#339966">كيفية عمل البرنامج؟</font></strong><br />
برنامج رانسيد عبارة عن سكريبتات تعمل على استخدام اسم مستخدم للدخول على أجهزة سيسكو و نقل الملفات إلى خادم رانسيد، لذلك يجب إعداد بعض الملفات قبل تشغيل البرنامج لتسهيل و تمكين البرنامج من الدخول إلى الأجهزة. بعد ذلك يتم وضع الملفات في نظام النسخ المتعدد CVS أو SVN لمعرفة التغييرات الطارئة على الملف و من ثم إرسالها إلى المستخدم.<br />
<br />
<br />
<strong><font color="#339966">ملخص الخطوات التي اتبعتها في إنشاء الخادم</font></strong><br />
أولا قمت بتثبيت حزمة رانسيد و من ثم إنشاء حساب مستخدم اسمه rancid<br />
بعد ذلك تعديل ملف إعدادات رانسيد الرئيسي rancid.conf و تغيير القيم التالية<br />
<code>LIST_OF_GROUPS="networks"</code><br />
<code>MAILDOMAIN="@yourdomain.tld"; export MAILDOMAIN</code><br />
ثم إنشاء الملف .cloginrc في المجلد الشخصي للمستخدم و في هذا الملف يجب إدخال معلومات الدخول الخاصة بكل راوتر أو سويتش أو فايروول.<br />
عمل روابط (ناعمة) soft links للسكريبتات ليسهل الوصول إليها، لا حاجة لعمل الروابط في حال وجود السكريبت rancid-run و rancid-cvs في المجلد /usr/local/bin/<br />
<code>ln -s /usr/local/libexec/rancid/clogin /usr/sbin/clogin
ln -s /usr/local/libexec/rancid/rancid-run /usr/local/bin/rancid-run
ln -s /usr/local/libexec/rancid/rancid-cvs /usr/local/bin/rancid-cvs</code><br />
بعد ذلك قمت بالدخول بحساب المستخدم rancid لتجربة الإعدادات في هذا الملف للتأكد من إمكانية الدخول للأجهزة و الحمد لله كانت الإعدادات تعمل بكفائة و بهذا تنتهي عملية إعداد رانسيد.<br />
بعد ذلك قمت بإعداد نظام النسخ المتعدد بإعطاء صلاحية كاملة للمستخدم الذي أنشأته على المجلد المخصص لذلك و هو /usr/local/var/rancid<br />
ثم قمت بكتابة الأمرين التاليين لتفعيل الـ CVS و تشغيل سكريبتات رانسيد<br />
<code>$ rancid-cvs
$ rancid-run</code><br />
الأمر الأول يقوم بإنشاء المجلدات الخاصة بنظام النسخ المتعدد و منها مجلد CVS و مجلد logs بالإضافة إلى مجلد بنفس الاسم الذي اخترته في LIST_OF_GROUPS و هو networks<br />
آخر خطوة قمت بعملها هي الدخول على المجلد networks و تعديل الملف router.db والذي قمت بإضافة الأجهزة التي أريد مراقبتها كما في الشرح المفصل<br />
بقي أمرين، أولها إرسال الرسائل عبر البريد الإلكتروني، و هذا يعتمد تماما على خادم البريد المستخدم، و بحكم أني أعمل على خادم بوستفيكس Postfix، فلقد قمت بالخطوات الموجودة في الشرح المفصل. أما الأمر الأخير هو جعل كل ما سبق تلقائي، و هذا يعني استخدام الـ cron<br />
<br />
<strong><font color="#339966">الخطوات بالتفصيل</font></strong><br />
<font color="#339966">تثبيت الحزمة:</font><br />
<code># cd /usr/ports/net-mgmt/rancid
# make install clean</code><br />
<br />
<font color="#339966">إنشاء حساب المستخدم و إعطاءه الصلاحيات اللازمة:</font><br />
<code># pw groupadd rancid
# pw useradd rancid -g rancid -m /home/rancid
# pw usermod -c "RANCID User fo Cisco Devices" -s /usr/local/bin/bash
# chown -R rancid:rancid /usr/local/var/rancid</code><br />
<br />
<font color="#339966">إعدادات الملف rancid.conf</font><br />
<code># cp -v /usr/local/etc/rancid/rancid.conf.sample /usr/local/etc/rancid/rancid.conf</code><br />
قمت بتعديل قيمة المتغيرات على النحو التالي:<br />
<code>LIST_OF_GROUPS="networks" 
MAILDOMAIN="@yourdomain.tld"; export MAILDOMAIN</code><br />
مع استبدال yourdomain.tld باسم النطاق الصحيح الذي استخدمه<br />
<br />
<font color="#339966">إعدادات الملف .clogin</font><br />
قمت بالدخول بحساب المستخدم rancid و إنشاء الملف .clogin في المجلد المنزلي Home Folder و إضافة المحتويات التالية:<br />
<code>add user 192.168.1.20     rancid</code><br />
هذا في حال استخدامك للمستخدم rancid في الدخول إلى أجهزة سيسكو، في حال استخدامك لمستخدم آخر، يجب وضع اسمه الصحيح هنا بدلا من rancid</p>
<p><br />
<code>add password 192.168.1.20     {verysecretpassword}     {enablepassword}
add method 192.168.1.20     ssh</code></p>
<p><br />
السطر الأول يعني استخدام كلمة المرور verysecretpassword للدخول إلى الجهاز المحدد 192.168.1.20 و كلمة المرور enablepassword للوضع المتقدم Enable Mode في جهاز سيسكو<br />
أما السطر الأخير فيعني استخدام بروتوكول ssh للدخول إلى الجهاز المعني و يمكن استبداله بـ telnet في حال عدم استخدامك للـ ssh، واعلم بأنك في وضع حرج!<br />
و في آخر الملف تأكد من وجود<br />
<code># set ssh encryption type, dflt: 3des
add cyphertype *</code><br />
<br />
و إن كان جهاز السيسكو الذي تستخدمه لا يحتاج إلى enable password يعني auto-enabled فيجب وضع السطر التالي قبل كلمة المرور<br />
<code>add autoenable 192.168.1.20 1</code><br />
<br />
<font color="#339966">تجربة الإعدادات في ملف .clogin</font><br />
قبل تجربة الإعدادات يفضل عمل الروابط (الناعمة) Soft Links لتسهل عملية كتابة الأوامر<br />
<code>ln -s /usr/local/libexec/rancid/clogin /usr/sbin/clogin
ln -s /usr/local/libexec/rancid/rancid-run /usr/local/bin/rancid-run
ln -s /usr/local/libexec/rancid/rancid-cvs /usr/local/bin/rancid-cvs</code><br />
و من ثم عملية التجربة<br />
<code>$ clogin 192.168.1.20</code><br />
إذا قام بالدخول إلى الجهاز و أعطاك سطر الأوامر الخاص بالسيسكو فالإعدادات صحيحة<br />
<br />
<font color="#339966">إعدادات نظام النسخ المتعدد</font><br />
بما أننا قمنا بإعطاء الصلاحيات اللزمة في خطوة إنشاء حساب المستخدم، بقي علينا تنفيذ الأمرين rancid-cvs و rancid-run مع مراعاة تنفيذها بالمستخدم rancid<br />
<code>$ rancid-cvs
$ rancid-run</code><br />
<br />
<font color="#339966">إعدادات router.db</font><br />
بعد تنفيذ الأمرين السابقين ستجد مجلدا بنفس القيمة التي اخترتها لـ LIST_OF_GROUPS و هي networks<br />
قم بالدخول إلى المجلد networks و تعديل الملف router.db بإضافة الأجهزة التي تريد مراقبتها<br />
<code>core1-sw-jed:cisco:up
core1-sw-riy:cisco:up
mpls-jed:cisco:up
192.168.1.20:cisco:up</code><br />
يمكنك وضع اسم الراوتر أو السويتش كما يمكنك وضع عنوان الأيبي الخاص به كما تلاحظون<br />
<br />
<font color="#339966">إعدادات خادم البريد</font><br />
إضافة السطر التالي في /usr/local/etc/postfix/virtual<br />
<code>rancid-networks     user@yourdomain.tld</code><br />
و من ثم postmap /usr/local/etc/postfix/virtual لإعتماد التغييرات في بوستفيكس. بهذه الخطوة، أي بريد موجه إلى rancid-networks سيقوم بوستفيكس بتوجيهه إلى user@yourdomain.tld<br />
<br />
<font color="#339966">إعدادات الـ cron</font><br />
و لقد قمت بالدخول بالمستخدم rancid و كتابة الأمر التالي لتعديل ملف الـ cron لهذا المستخدم<br />
<code>$ crontab -e</code><br />
و من ثم إضافة السطرين التاليين:<br />
<code># Run config differ every hour
0 * * * * /usr/local/bin/rancid-run
# Clean out config differ logs (+n keeps n days, so 2 here) at 3:00AM
0 3 * * * /usr/bin/find /usr/local/var/rancid/logs -type f -mtime +2 -exec rm {} \;</code><br />
<br />
<br />
<font color="#339966">المصادر التي استفدت منها في الموضوع</font><br />
<a href="http://www.joe-ma.co.za/page.php?9">http://www.joe-ma.co.za/page.php?9</a><br />
<a href="http://www.bsdguides.org/guides/freebsd/networking/rancid">http://www.bsdguides.org/guides/freebsd/networking/rancid</a><br />
<a href="http://homepage.mac.com/duling/halfdozen/RANCID-Howto.html#d0e395">http://homepage.mac.com/duling/halfdozen/RANCID-Howto.html#d0e395</a></p>
