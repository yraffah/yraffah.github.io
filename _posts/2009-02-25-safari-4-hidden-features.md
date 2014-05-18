---
layout: post
title: !binary |-
  2K7Ytdin2KbYtSDYs9mB2KfYsdmKIDQg2KfZhNmF2K7ZgdmK2Kk=
created: 1235565783
---
<div class="rtecenter"><a href="http://www.apple.com/safari"><img width="410" height="320" alt="" src="http://bandar.raffah.com/wp/wp-content/uploads/2009/02/overview-hero-image1-20090217-1.jpg" /></a></div>
&nbsp;طرحت أبل الإصدار التجريبي من برنامجها متصفح الإنترنت سفاري يوم أمس وقد تحدث <a href="http://bandar.raffah.com/wp/?p=1527">بندر رفه</a> بشكل سريع عن خصائصه الجديدة. لكن اليوم موضوعنا مختلف قليلا لأني سأشرح لكم بعض الخصائص المخفية للمتصفح والتي قد تسائل بعضكم عنها. منها على سبيل المثال شريط الـ <span style="font: 12.0px Lucida Grande">Tab</span> <span style="font: 12.0px Lucida Grande">Bar</span> و وجوده في أعلى المتصفح حيث<span style="font: 12.0px Lucida Grande"> </span>تسائل<span style="font: 12.0px Lucida Grande"> </span>البعض<span style="font: 12.0px Lucida Grande"> </span>كيف<span style="font: 12.0px Lucida Grande"> </span>يمكن<span style="font: 12.0px Lucida Grande"> </span>أن<span style="font: 12.0px Lucida Grande"> </span>نتأقلم<span style="font: 12.0px Lucida Grande"> </span>على<span style="font: 12.0px Lucida Grande"> </span>ذلك<span style="font: 12.0px Lucida Grande">.</span>
<p dir="rtl" style="margin: 0.0px 0.0px 0.0px 0.0px; text-align: right; font: 12.0px Geeza Pro">في<span style="font: 12.0px Lucida Grande"> </span>هذا<span style="font: 12.0px Lucida Grande"> </span>الموضوع<span style="font: 12.0px Lucida Grande"> </span>سأريكم كيف يمكن أن تغييروا من مكان الـ <span style="font: 12.0px Lucida Grande">Tab</span> <span style="font: 12.0px Lucida Grande">bar</span> إلى مكانه الأصلي والذي اعتدتم عليه بالإضافة إلى عدة خصائص أخرى.&nbsp;ولكن قبل أن نبدأ يجب أن تعلموا بأن هذه الأوامر تكتب في برنامج <span style="font: 12.0px Lucida Grande">Terminal</span> والموجود ضمن المجلد <span style="font: 12.0px Lucida Grande">Applications</span> > <span style="font: 12.0px Lucida Grande">Utilities<br />
<br />
<strong> ملاحظة:&nbsp;بعد كتابة أي من هذه الأوامر يجب إعادة تشغيل السفاري لرؤية التغييرات.</strong><br />
<br />
</span></p>
<p dir="rtl" style="margin: 0.0px 0.0px 0.0px 0.0px; text-align: right; font: 12.0px Geeza Pro">استعادة شريط التابز بالشكل القديم <span style="font: 12.0px Lucida Grande">Tab</span> <span style="font: 12.0px Lucida Grande">Bar<br />
<div dir="ltr"><code>
$ defaults write com.apple.Safari DebugSafari4TabBarIsOnTop -bool NO 
</code></div>
<br />
</span></p>
<p dir="rtl" style="margin: 0.0px 0.0px 0.0px 0.0px; text-align: right; font: 12.0px Geeza Pro">استعادة<span style="font: 12.0px Lucida Grande"> </span>الشريط الأزرق الذي يبين تحميل الصفحة والترس المتحرك أو <span style="font: 12.0px Lucida Grande">Loading Spinner </span>في نفس الـ <span style="font: 12.0px Lucida Grande">Tab<br />
<br />
<div dir="ltr"><code>
$ defaults write com.apple.Safari DebugSafari4IncludeToolbarRedesign -bool NO
$ defaults write com.apple.Safari DebugSafari4LoadProgressStyle -bool NO 
</code></div>
<br />
</span></p>
<p dir="rtl" style="margin: 0.0px 0.0px 0.0px 0.0px; text-align: right; font: 12.0px Geeza Pro">لإلغاء عملية التكملة التلقائية لعنوان الـ <span style="font: 12.0px Lucida Grande">URL<br />
<br />
<div dir="ltr"><code>
$ defaults write com.apple.Safari DebugSafari4IncludeFancyURLCompletionList -bool NO
</code></div>
<br />
</span></p>
<p dir="rtl" style="margin: 0.0px 0.0px 0.0px 0.0px; text-align: right; font: 12.0px Geeza Pro">لإلغاء إقتراحات جووجل <span style="font: 12.0px Lucida Grande">Google</span> <span style="font: 12.0px Lucida Grande">Suggest<br />
<br />
<div dir="ltr"><code>
$ defaults write com.apple.Safari DebugSafari4IncludeGoogleSuggest -bool NO
</code></div>
<br />
</span></p>
<p dir="rtl" style="margin: 0.0px 0.0px 0.0px 0.0px; text-align: right; font: 12.0px Geeza Pro">لإلغاء <span style="font: 12.0px Lucida Grande">CoverFlow</span> من الـمفضلة أو الـ <span style="font: 12.0px Lucida Grande">Bookmarks<br />
<br />
<div dir="ltr"><code>
$ defaults write com.apple.Safari DebugSafari4IncludeFlowViewInBookmarksView -bool NO
 </code></div>
<br />
</span></p>
<p dir="rtl" style="margin: 0.0px 0.0px 0.0px 0.0px; text-align: right; font: 12.0px Geeza Pro">لإلغاء التعتيم عند الضغط على أفضل المواقع <span style="font: 12.0px Lucida Grande">Top</span> <span style="font: 12.0px Lucida Grande">Site</span> لتكبير لقطة الشاشة و ملئ شاشة العرض</p>
<div dir="ltr"><code>
$ defaults write com.apple.Safari DebugSafari4TopSitesZoomToPageAnimationDimsSnapshot -bool NO
 </code></div>
<br />
<p dir="rtl" style="margin: 0.0px 0.0px 0.0px 0.0px; text-align: right; font: 12.0px Geeza Pro">لإلغاء خاصية أفضل<span style="font: 12.0px Lucida Grande"> </span>المواقع<span style="font: 12.0px Lucida Grande"> Top Sites </span>بشكل<span style="font: 12.0px Lucida Grande"> </span>كامل</p>
<div dir="ltr"><code>
$ defaults write com.apple.Safari DebugSafari4IncludeTopSites -bool NO 
</code></div>
<br />
<p dir="rtl" style="margin: 0.0px 0.0px 0.0px 0.0px; text-align: right; font: 12.0px Geeza Pro">و<span style="font: 12.0px Lucida Grande"> </span>لاستعادة<span style="font: 12.0px Lucida Grande"> </span>أي من الخصائص مرة أخرى يمكنكم كتابة التالي:</p>
<div dir="ltr"><code>
$ defaults delete com.apple.Safari <key>
</code></div>
<br />
مع استبدال <key> بـ أي من المتغييرات المطلوب استعادتها و هي موجودة في الأسفل. <br />
<div dir="ltr"><code>DebugSafari4TabBarIsOnTop
DebugSafari4IncludeToolbarRedesign 
DebugSafari4IncludeFancyURLCompletionList
DebugSafari4IncludeGoogleSuggest
DebugSafari4LoadProgressStyle
DebugSafari4IncludeFlowViewInBookmarksView
DebugSafari4TopSitesZoomToPageAnimationDimsSnapshot
DebugSafari4IncludeTopSites </code></div>
&nbsp;<br />
<br />
بالنسبة لمستخدمي سفاري 4 على الويندوز يمكنكم تحميل البرنامج <a href="http://www.ipodrobot.com/download.htm">plist editor</a> لتحرير الملف<br />
<div dir="ltr">
<code>
C:\Documents and Settings\your username here\Application Data\Apple Computer\Preferences\com.apple.Safari
</code>
</div><br />
<p>&nbsp;</p>
المصدر::Source<br />
<a href="http://swedishcampground.com/safari-4-hidden-preferences">http://swedishcampground.com/safari-4-hidden-preferences</a><br />
<p>&nbsp;</p>

</key>
