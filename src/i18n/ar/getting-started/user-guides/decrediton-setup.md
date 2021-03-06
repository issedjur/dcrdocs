# دليل إعداد Decredition

اخر تحديث له كان v1.0.0.

---

`Decrediton` الواجهة الرسومية للمستخدم `dcrwallet`. عندما تطلق هذا التطبيق، فإنه يبدأ تلقائيا بمثيلتها الخاصة `dcrd` و `dcrwallet` وخلفيتهما - وهكذا فهي سوف تفتح وستحتوي على نظام تشغيل  `dcrd`.

ملاحظة: اذا حصل خلال أي نقطة في البرنامج أن علق التحميل أو لم يستجب, عادة ما يتم إصلاح ذلك من خلال إعادة تشغيل التطبيق.

---

## تحميل وتثبيت

Decrediton is released with the Binary Releases and can be found here: [https://github.com/decred/decred-binaries/releases/tag/v1.1.0](https://github.com/decred/decred-binaries/releases/tag/v1.1.0). As of v1.1.0, Decrediton is only available for Linux and macOS.

> macOS

1. Download the `decrediton-1.1.0.dmg` file.

2. Double click the `decrediton-1.1.0.dmg` file once downloaded to mount the disk image.

3. اسحب تطبيق decrediton.app إلى الرابط الخاص بتطبيقك بدون صورة القرص.

> Linux

1. Download the `decrediton-1.1.0.tar.gz` file.

2. إنتقل إلى تحميل الموقع وإستخرج .tar.gz file:

   أوبونتو متصفح الملفات: ببساطة انقر بزر الماوس الأيمن على .tar.gz وحدد "استخراج هنا" <br />
   محطة: إستخدم أمر `tar -xvzf filename.tar.gz` .

    Both of these should extract the tar.gz into a folder that shares the same name. (`e.g. tar -xvzf decrediton-v1.1.0.tar.gz` should extract to `decrediton-v1.1.0`). If successful, this new folder should include a `decrediton` executable.

---

## المعلومات الهامة

خلال إنشاء هذا العمل في محفظتك, فإنه سيتم إعطائك تسلسل مكون من 33 كلمة تعد كما لو أنها عبارة ذات أصول. وهذا العبارات ذات الأصول تعد بشكل أساسي كالمفتاح الخاص بمحفظتك. وإنك سوف تكون قادر على إستخدام هذه الأصول لإستعادة مفاتيحك الخاصة, تاريخ المعاملات، والأرصدة باستخدام أي محفظة Decred على أي جهاز حاسوب.

وهذا يعني في نهاية المطاف *أن أي شخص* يعرف الأصول الخاصة بك يمكنه إستعادة مفاتيحك الخاص, تاريخ المعاملات, والأرصدة لمحفظة Decred على جهازه الخاص دون معرفتك بهذا الأمر. ولهذا السبب, يعد من المهم المحافظة على محفظتك بشكل سري وأمن. حيث أن حماية هذه الأصول يحتاج لنفس طريقة حماية المفتاح الأساسي. بحيث إنك إن فقدت هذاه الأصول, فانك تلقائيا سوف تفقد القدرة على الدخول الى محفظتك والأسهم الخاصة بك. ولا يمكن إستعادتها حتى لو إستعنت بمؤسسي Decred. لذلك فإن من الأفضل لك تخزينه في مكان أمن. وإن قمت بتفضيل حفظه على جهازك الخاص, فانه من الأفضل لك حفظه في الملفات المشفره (مع عدم نسيان كلمة المرور) في حال تعرض الملف أو الحاسوب للسرقة.

**تذكير: لا, تخضع لأي من أوامر إعطاء أصولك أو الأصول المعرفية لأي شخص, حتى لو كان أحد المسؤولين!**

---

## إنشاء محفظة جديدة

بعد قيامك بالضغط على "حسنا, لقد فهمت" وذلك لإخلاء المسؤولية, فإنك سوف ترى حوار " إنشاء المحفظة".

الحوار الإفتراضي "لإنشاء المحفظة" من خلال "أصول جديدة" تعد إختيارية. يمكن النقر ببساطة على "قائمة الأصول" إلا إن كان لديك في الأصل ما تنوي إستخدامه, يمكنك حينها إتباع الخطوات المدرجة. حيث أن هذا الدليل يفترض أنه ليس لديك أصول وأنك سوف تختار "الأصول الجديدة". لذلك قم بمراجعة  [المعلومات الهامة](#critical-information) حول الأصول السابقة.

1. قم بتسجيل الأصول التي تم عرضها في النص (حيث أنك سوف تحتاج لإعادة النقر على الشاشة التالية).

2. أنقر "متابعة"

3. قم بتأكيد أصولك, وإنشاء عبارة مرور لمحفظتك. حيث أن عبارة المرور هذه قد تستخدم لإلغاء قفل محفظتك عند إنشاءك المعاملات.

4. أنقر "إنشاء المحفظة"

5. ثم يجب أن ترى الدائرة الزرقاء. بحيث تم مزامنت `dcrd` بشكل تسلسل الكتل الكاملة. في أجهزة الحاسوب التي لا تحتوي على `dcrd` المحملة عليها, وعادة ما تستغرق من 1-2 ساعات إن كانت الأجهزة حديثة (بحيث أنها سوف تستغرق وقت أطول في الأجهزة الأقدم). يمكنك التحقق من تطبيق مراقبة العملية لمثيل تشغيل `dcrd` -  إذا قمت بإستخدام نسبة كبيرة خاصة من CPU الخاصة بك. وان لم يتم ذلك فإنك, لن تحتاج لطلب إعادة البدء للتحرك خلال هذه الشاشة.

## إفتح محغظتك

بعد أن يكون تسلسل الكتل قد تمت مزامنته, نجد أنك قد تستطيع رؤية صفحة "فتح المحفظة". وهنا, يمكنك ملاحظة إمكانية إدخال كلمة المرور الخاصة بك وسوف تقوم المحفظة باعادة فحص الكتل الأخيرة للمعاملات التي تنتمي إلى عناوينك. انتظر حتى يتم ملء شريط التقدم. ثم قم بتحميل Decrediton اي الصفحة ذات النظرة العامة للرصيد المتاح والمعاملات الأخيرة المعروضة.

---
