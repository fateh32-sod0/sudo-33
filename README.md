# sudo-33
Fateh-kehila-hack

termux-سودو
يعد البرنامج النصي bash الذي يوفر sudo لـ Termux
Termux محاكيًا طارئًا وبيئة Linux لنظام Android

ملحوظة

تم استضافة termux-sudo في الأصل على GitHub.
نظرًا لحقيقة حذف Termux sudo من Github ، فقد قررت تحميله لمتطلبات الاستخدام العام

الهاتف الجذر مع سو
سودو ثنائي لن تعمل دون سو

تثبيت sudo

استنساخ termux-sudo أو قم بتنزيله على الهاتف واستخرجه
فتح Termux
تثبيت التبعية اللازمة ل sudo: pkg install ncurses-utils
التغيير إلى دليل الاستنساخ أو الاستخراج
تنفيذ الأوامر التالية لوضع sudo في الدليل الصحيح مع الأذونات المناسبة والملكية
cat sudo > /data/data/com.termux/files/usr/bin/sudo
chmod 700 /data/data/com.termux/files/usr/bin/sudo
المميزات

إعداد بيئتها تلقائيًا عند التشغيل لأول مرة ، ولا حاجة إلى القيام بأي شيء سوى استخدامه
إنشاء مجلد جذر .surootفي المجلد الرئيسي Termux مع أذونات الجذر المناسبة والملكية
لإنشاء .bashrcملف في مجلد جذر باستخدام متغيرات PATH و LD_LIBRARY_PATH المناسبة حتى تعمل جميع الثنائيات بشكل صحيح
Bash موجه PS1 متغير هو أيضا مجموعة حتى لا يكون لديك bash-4.4#موجه فقط#
يتم إنشاء .bash_historyمجلد الجذر تلقائيًا عند إسقاطه إلى قشرة جذر بحيث يتم الاحتفاظ بمحفوظات قشرة الجذر
يمكن استخدامها مثل sudo العادي (ولكن فقط كجذر ، لا مستخدم آخر)
يمكن أن تنخفض إلى جذر قذيفة sudo su [-]
يعمل في ثنائيات Termux والثنائيات الخارجية مع الوسائط الاختيارية كجذر في الدليل الحالي
يولد الإخراج في قذيفة تستخدم حاليا
يمكن استخدامها في البرامج النصية باش الأخرى
[الخيار] يمكن إيقاف رسائل الخطأ الملونة يكون تحرير المتغير coloredفي بداية ملف sudo
Usage:

sudo su [-]  
  Drop to root shell

sudo <command> [<args>]  
  Run command as root with optional arguments
استلهم هذا ما يلي: https://github.com/st42/termux-sudo https://github.com/cswl/tsu
https://gist.github.com/cswl/cd13971e644dc5ced7b2
