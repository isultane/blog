---
layout: post
title: التدوينه الثالثه!
---
![Image result for blockchain](./media/image1.png)

**<span dir="rtl">ماهوالـ</span> Blockchain <span dir="rtl">؟</span>**

<span dir="rtl">إعداد</span>

<span dir="rtl">د. سلطان بن سعود القحطاني</span>

<span dir="rtl">أستاذ مساعد بكلية علوم الحاسب والمعلومات</span>

<span dir="rtl">جامعة الإمام محمد بن سعود الإسلاميه</span>

<span dir="rtl">  
</span>

# <span dir="rtl">مقدمة</span>

<span dir="rtl">أود ان اوضح بأن تقنية الـ</span> Blockchain
<span dir="rtl">هي مفهوم بسيط وسهل جدا لمن لديهم مفهوم هندسة البرمجيات
وتطوير البرامج. الـ</span> Blockchain <span dir="rtl">هي مفهوم من
مفاهيم تراكيب البيانات (</span>Data Structure<span dir="rtl">)
وبالطبع مفهوم الـ</span> Cryptocurrency <span dir="rtl">يعتبر مفهوم
معقد ولاكن تقنية الـ</span> Blockchain <span dir="rtl">ليست السبب في
ذلك. السبب في ان مفهوم الـ</span> Cryptocurrency
<span dir="rtl">معقده هو ما تحتويه من خوارزميات
(</span>Algorithms<span dir="rtl">) خاصة بالتنقيب
(</span>Mining<span dir="rtl">) ونقصد بالتنقيب هنا هو الـ</span> Bitcoin
mining<span dir="rtl">,ايضا في تعقيد مفهوم الـ</span> Cryptocurrency
<span dir="rtl">هو ما يرتبط بها من العمليات الحسابيه وتوزيعها, مفهوم
الـ</span> Ledger <span dir="rtl">(او مايعرف بالمحفظة الماليه
بالمفهوم العام).</span>

<span dir="rtl">قبل ان نبدأ في شرح تقنية الـ</span> Blockchain
<span dir="rtl"> وكيفية عملها, تحتاج ان تتعرف على مفهوم الـ</span> Hash
<span dir="rtl">ولماذا هو مهم في تقنية الـ</span>
Blockchain<span dir="rtl">.</span>

<span dir="rtl">الـ</span> Hash <span dir="rtl">في الحقيقه هو مفهوم
مشابه لمفهوم التوقيع الرقمي (</span>Digital
Signature<span dir="rtl">) أو كمن تعطي شيء صفة خاصه به تميزه عن غيره مثل
رقم بطاقة الأحوال (</span>Digital ID<span dir="rtl">). مثلا ممكن نأخذ
ملف فلم أو نص أو صوره ونعمل له</span> Hash <span dir="rtl">ويصبح لهذا
الملف رقم خاص به أو</span> Digital ID<span dir="rtl">, ايضا ممكن نأخذ
بريد إلكتروني ونعمل له</span> Hash <span dir="rtl">ويصبح هذا الهاش هو
الرقم الخاص بهذا البريد الإلكتروني.  مثال الصورة التالية:</span>

> ![https://lh4.googleusercontent.com/nxV7D7DkDMbhf401qCFvCF3Kfqzqf5vJ6eQ1fLyfRD5DoC9MaM8a7NZxZXIXcxnDVDdisVfedmFQGhkOTP21K4UKbBGIP1dSkaBgEKDCfA8rwrVnn2tIdScf3MUY8ANtQGefWBhn](./media/image2.png)

<span dir="rtl">عبارة عن ملف نصي, عملنا له</span> Hash
<span dir="rtl">وسيخرج رقم عشوائي وهذا الرقم هو</span> Digital ID
<span dir="rtl">لهذا الملف النصي واللذي يكون مميز عن غيره. لكي اتحقق بأن
هذا الملف النصي صحيح لابد ان يكون الـ</span> Digital ID
<span dir="rtl">مطابق. لو اخذنا المثال التالي:</span>

String\[\] list1 = {"a", "b", "c"};

String\[\] list2 = {"a", "b", "c"};

<span dir="rtl">عباره قائمتن (</span>two lists<span dir="rtl">), القائمه
الأولى (</span>list1<span dir="rtl">) تحتوي على</span> "a", "b", "c"
<span dir="rtl">بينما القائمه الثانيه (</span>list2<span dir="rtl">)
تحتوي على</span> "a", "b", "c"<span dir="rtl">. محتوى القائمتين
عباره عن بيانات وكل قائمه عباره عن بيانات خاصه بها</span>
<span dir="rtl">لكن المحتوى متشابه. لو قمنا بصناعة</span> Digital ID
<span dir="rtl">خاص بها ماذا سيحدث؟</span>

String\[\] list1 = {"a", "b", "c"};

String\[\] list2 = {"a", "b", "c"};

System.out.println(Arrays.hashCode(list1));

System.out.println(Arrays.hashCode(list2));

<span dir="rtl">نلاحظ ان المخرجات لكل عملية طباعه ستكون متطابقه على
النحو التالي:</span> **126145** <span dir="rtl">وهو يمثل الـ</span>
Digital ID <span dir="rtl">أو الـ</span> Digital signature
<span dir="rtl">للبيانات في الـ</span> list1 <span dir="rtl">و</span>
**126145** <span dir="rtl">لـ</span>list2 <span dir="rtl">نفس الشيء. لو
قمنا بتعديل محتوى</span> list2 <span dir="rtl"> مثلا إلى:</span>

String\[\] list1 = {"a", "b", "c"};

String\[\] list2 = {"a", "b", "c"};

System.out.println(Arrays.hashCode(list1));

System.out.println(Arrays.hashCode(list2));

<span dir="rtl">ستكون المخرجات مختلفه على النحو التالي:</span> 126145
<span dir="rtl">لـ</span> list1 <span dir="rtl">و</span> 126642
<span dir="rtl">لـ</span> list2<span dir="rtl">, فبالتالي إذا عملنا
تغيير بسيط على أحد المحتويات في القئمتين الموضحه في المثال سوف نحصل
على</span> Digital signature <span dir="rtl">مختلف تماما عن السابق, وهذا
هو الأساس المبني عليه تقنية الـ</span>Blockchain
<span dir="rtl">.</span>

<span dir="rtl">لأن الـ</span> Blockchain <span dir="rtl">هي عبارة عن
قائمه (</span>list<span dir="rtl">) من الـ</span> Blocks
<span dir="rtl">أو في الأساس سلسله (</span>chain<span dir="rtl">) من
الـ</span> Blocks <span dir="rtl">وكل</span> Block
<span dir="rtl">يحتوي على التالي: 1- مجموعه من الـ</span>
Transactions <span dir="rtl">(العمليات اللتي تمت في هذا الـ</span>Block
<span dir="rtl">) و 2-</span>Digital ID <span dir="rtl">أو</span>
Signature <span dir="rtl">خاص فيه و 3-</span> Digital signature
<span dir="rtl">خاص بالـ</span> Block <span dir="rtl">اللذي قبل.كما هو
مبين في الصوره التاليه:</span>

![Image result for blockchain hash](./media/image3.png)

<span dir="rtl">أي بمعنى أن الـ</span> Blocks <span dir="rtl">في السلسله
معتمدين على بعض, فبالتالي, الـ</span> Digital ID
<span dir="rtl">لأي</span> Block <span dir="rtl">في السلسلة معتمد على
الـ</span> Digital ID <span dir="rtl">للبلوك اللذي قبله. إذا غيرنا في اي
محتوى</span> Block <span dir="rtl">(اي غيرنا على البيانات</span>
<span dir="rtl">الخاصه بالـ</span>Block <span dir="rtl">) في السلسله,
فهذا يعني اننا اثرنا على جميع الـ</span>Blocks
<span dir="rtl">المرتبطه في السلسله.</span>

<span dir="rtl">بعد ماتعرفنا على مفهوم الـ</span>Hash
<span dir="rtl">وارتباطه بتقنية الـ</span>Blockchain<span dir="rtl">,
في القسم التالي سنبني برنامج بسيط يشرح كيفية برمجة الـ</span> Blockchain
<span dir="rtl">بإستخدام لغة</span> Java<span dir="rtl">.</span>

<span dir="rtl">  
</span>

# <span dir="rtl">تطبيق الـ</span> Blockchain <span dir="rtl">بأستخدام لغة</span> Java <span dir="rtl">؟</span>

<span dir="rtl">في البداية اول شيء نتحدث عنه في تركيبة الـ</span>
Blockchain <span dir="rtl"> هو الـ</span> Block <span dir="rtl">وماذا
يحتوي. في هذا المثال كما هو موضح في الصوره التاليه</span>:

<span dir="rtl">في هذا المثال, الـ</span> Block <span dir="rtl"> اللذي
سنبنيه بسيط جدا ويحتوي على ثلاث اشياء رئيسية: 1- قائمة من العمليات
(</span>transactions<span dir="rtl">) اللتي تمت من خلال هذا
الـ</span>Block <span dir="rtl">, 2- قيمة الـ</span> Hash
<span dir="rtl">السابق (قيمة الـ</span>Hash <span dir="rtl">الخاص
بالـ</span>Block <span dir="rtl">المرتبط بالـ</span>Block
<span dir="rtl">الحالي), 3- الـ</span>Hash <span dir="rtl">الخاص
بالـ</span>Block <span dir="rtl">الحالي. بالنسبه للعنصر رقم 3,
القيمه الخاصه بهذا الـ</span>Hash <span dir="rtl">ستكون مبنية على
قيمة الـ</span>list <span dir="rtl">و الـ</span> Hash
<span dir="rtl">السابق, اي ان قيمة الـ</span> Digital ID
<span dir="rtl">ستكون محسوبه بناء على العمليات اللتي تمت في الـ</span>
Block <span dir="rtl">الحالي و اضافة على قيمة الـ</span> Hash
<span dir="rtl">الخاص بالـ</span>Block <span dir="rtl">السابق. فإذا قام
شخص ما بتغيير محتوى</span> Block <span dir="rtl">السابق فهذا يعني أن
الـ</span> Block <span dir="rtl">الحالي سوف يتغير بناء على التغييرات
السابقه, وايضا الـ</span>Block <span dir="rtl">اللذي يليه سوف يتغير
وهكذا. لنتعرف سوية على كيفية عمل هذا الكلام النظري بـ</span>code
<span dir="rtl"> يترجم هذا المفهوم.</span>

**public** **class** Block {

**private** **int** previousHash;

**private** String\[\] transactions;

**private** **int** blockHash;

...

}

<span dir="rtl">نصنع</span> Class <span dir="rtl">ونطلق عليه اسم</span>
Block <span dir="rtl">ويحتوي هذا الـ</span>Class <span dir="rtl"> على
العناصر التاليه:</span> previousHash<span dir="rtl">,</span>
transactions<span dir="rtl">,</span> blockHash<span dir="rtl">.
الـ</span> transactions <span dir="rtl"> في هذا المثال فقط استخدمنا
مصفوفه من النصووص (</span>Strings<span dir="rtl">) لتوضيح المفهوم
ومحاولة صنع</span> Blockchain <span dir="rtl">بمثال بسيط. بينما في
الأمثله الحقيقه والتطبيقات الخاصه بالـ</span>Blockchain
<span dir="rtl">فالـ</span> transactions <span dir="rtl">تكون اكبر من
مجرد مصفوفة نصوص, بل تتكون من تراكيب بيانات واشياء تعتمد على طبيعة
البرنامج او النظام اللذي صمم له الـ</span>
Blockchain<span dir="rtl">.</span>

<span dir="rtl">عند بناء</span> Objects <span dir="rtl">لـ</span>Block
<span dir="rtl">معين, نطبق المفوم المرتبط بالعنصر رقم 3, وستكون دالة
الـ</span>constructor <span dir="rtl">كالتالي:</span>

**public** Block(**int** previousHash, String\[\] transactions) {

**this**.previousHash = previousHash;

**this**.transactions = transactions;

Object\[\] contents = {Arrays.*hashCode*(transactions), previousHash};

**this**.blockHash = Arrays.*hashCode*(contens);

}

<span dir="rtl">نلاحظ هنا انه عند انشاء</span>Block <span dir="rtl">
معين, يكون الـ</span> Hash <span dir="rtl">الخاص به عبارعن المحتوى
(</span>contents<span dir="rtl">) الخاص بالـ</span>Block
<span dir="rtl">نفسه واللذي هو عباره عن الـ</span>Hash
<span dir="rtl">الخاص بالـ</span>transactions
<span dir="rtl">(</span>Arrays.*hashCode*(transactions)<span dir="rtl">)
اللذي تم في هذا الـ</span> Block <span dir="rtl"> و قيمة الـ</span>Hash
<span dir="rtl"> الخص بالـ</span>Block <span dir="rtl">السابق
(</span>previousHash<span dir="rtl">). وبالتالي أي تغيير في احدى
القيميتين سيحدث تأثير على قيمة الـ</span>Blocks
<span dir="rtl">المرتبطه بهذا الـ</span>Block <span dir="rtl">. اخيرا,
لكل</span> Block <span dir="rtl">يوجد مجموعة دوال لإسترجاع المعلومات
الخاصه بالـ</span> Block <span dir="rtl">وهي:</span>
getPreviousHash()<span dir="rtl">,</span>getTransaction()<span dir="rtl">,</span>getBlockHash()
<span dir="rtl"> وجميعها دوال فقط تستخدم في حالة البناء
للـ</span>Blockchain <span dir="rtl">. وبالتالي يصبح شكل
الـ</span>Class Block <span dir="rtl">بعد بناء جميع الدوال والعناصر
المكونه للـ</span> Block <span dir="rtl">كالتالي:</span>

**public** **class** Block {

**private** **int** previousHash;

**private** String\[\] transactions;

**private** **int** blockHash;

**public** Block(**int** previousHash, String\[\] transactions) {

**this**.previousHash = previousHash;

**this**.transactions = transactions;

Object\[\] contents = {Arrays.*hashCode*(transactions), previousHash};

**this**.blockHash = Arrays.*hashCode*(contens);

}

**public** **int** getPreviousHash() {

**return** previousHash;

}

**public** String\[\] getTransaction() {

**return** transactions;

}

**public** **int** getBlockHash() {

**return** blockHash;

}

}

<span dir="rtl">بعد أن انتهينا من بناء</span>class Block
<span dir="rtl">, تأتي الان طريقة بناء الـ</span>Blockchain
<span dir="rtl">, واللتي هي عباره عن سلسله
(</span>chain<span dir="rtl">) من الـ</span>Blocks<span dir="rtl">. اي
اننا نحتاج نوع من انواع تراكيب البيانات (</span>Data
structure<span dir="rtl">) تساعدنا في بناء هذه السلسله. في لغة جافا
سنستخدم</span> ArrayList <span dir="rtl">لسبب بسيط هو سهولة
الإستخدام والتعامل معها وبإمكانك تستخدم</span> LinkedList,
Vecotr <span dir="rtl">وغيرها, اهم شيء لابد ان تكون بيانات على شكل
سلسله. ولتعريف الـ</span>ArrayList <span dir="rtl">نقوم
بالتالي:</span>

ArrayList\<Block\> *blockchain* = new ArrayList();

<span dir="rtl">كما نلاحظ بأن الـ</span> blockchain <span dir="rtl">هو
عباره عن</span> object <span dir="rtl">من نوع مصفوفه متسلسله وكل عنصر
فيها يمثل</span> Block <span dir="rtl">لذلك عملنا</span>
ArrayList\<Block\><span dir="rtl">.</span>

<span dir="rtl">ذكرت سابقا بأن كل</span> Block <span dir="rtl">مرتبط
في</span> Block <span dir="rtl">اخر مما يكون شكل سلسلة, وايضا بناء
الـ</span>Hash <span dir="rtl">لكل</span>Block <span dir="rtl">مرتبط
بالـ</span>Blcok <span dir="rtl">السابق, لكن السؤال هنا هو ماذا عن
الـ</span>Block <span dir="rtl">الأول في السلسلة؟ كيف يتم بناء
الـ</span> Hash <span dir="rtl">الخاص به إن لم يكون هناك قيمه
لـ</span> Hash <span dir="rtl">سابقه. بالنسبة للـ</span>Block
<span dir="rtl">الأول في الـ</span>Blockchain <span dir="rtl">يطلق
عليه</span> Genesis Block <span dir="rtl">فالبالتالي جميع مكوناته
تبنى من الصفر والـ</span>Hash <span dir="rtl">الخاص به يكون مبني
على</span> Hash <span dir="rtl">سابق عشوائي. كالمثال التالي:</span>

String \[\] genesisTransactions = {"Sultan sent Feras 10 bitcoin","Feras
sent 100 bitcoins to Hamad"};

Block genesisBlock = **new** Block(0, genesisTransactions);

*blockchain*.add(genesisBlock);

<span dir="rtl">ولغرض التبسيط في هذا المثال, صنعنا</span>
genesisTransactions <span dir="rtl"> وهي عباره عن مصفوفة نصوص
(</span>strings<span dir="rtl">) تمثل عمليات عشوائيه (</span>fake
transactions<span dir="rtl">) وبدورها تمثل العمليات اللتي تمت في
الـ</span> Genesis Block<span dir="rtl">.</span>
<span dir="rtl">وقمنا بصناعة الـ</span>Genesis Block
<span dir="rtl">وكما نلاحظ طالما انه ليس لديه</span> Block
<span dir="rtl">سابق, فالبالتالي الـ</span> Hash <span dir="rtl">السابق
سيكون عباره عن صفر (</span>zero<span dir="rtl">) وبأمكانك ان تضع قيمه
عشوائيه اخرى, المهم بأن هذا الـ</span>Block <span dir="rtl">في حالة
صناعة المحتوى الخاص به لا يرتبط بمحتوى</span> Block
<span dir="rtl">اخر, وهذا يعني ان الـ</span> Hash
<span dir="rtl">الخاص به يعتمد إعتماد كلي على طريقتك في صناعته. بعد
صناعة الـ</span> Block <span dir="rtl">الأول نقوم بإضافته في</span>
*blockchain <span dir="rtl"> </span>*<span dir="rtl">اللذي صنعناه في
البدايه. لوقمنا بطباعة محتوى الـ</span> Hash <span dir="rtl">الخاص
بهذا الـ</span> Block <span dir="rtl">نقوم بالتالي:</span>

System.*out*.println("Hash of genesis block:");
System.*out*.println(*blockchain*.get(0).getBlockHash());

<span dir="rtl">المخرجات ستكون كالتالي:</span>

Hash of genesis block:

\-325325674

<span dir="rtl">نلاحظ بأن الرقم</span> 325325674<span dir="rtl">- عباره
عن قيمة الـ</span>Hash <span dir="rtl">الخاص بالـ</span>Genesis
Block<span dir="rtl">, ومثل ماشفنا في طريقة بناء الـ</span> Hash
<span dir="rtl">لكل</span> Block <span dir="rtl">بأنه يعتمد على محتوى
الـ</span> Block <span dir="rtl">نفسه (يمثله العمليات</span>
transactions <span dir="rtl">اللي تمت في نفس</span>
Block<span dir="rtl">), أي بمعنى انه اذا تغير اي شيء في
الـ</span>transactions <span dir="rtl">سيؤثر على قيمة الـ</span>
Hash<span dir="rtl">, مثلا:</span>

String \[\] genesisTransactions = {"Sultan sent Feras
<span dir="rtl">20</span> bitcoin","Feras sent <span dir="rtl">50</span>
bitcoins to Hamad"};

Block genesisBlock = **new** Block(0, genesisTransactions);

*blockchain*.add(genesisBlock);

<span dir="rtl">قمنا بتغيير العمليتين التاليه: عوضا ان يرسل سلطان لفراس
قيمه 10 بتكوين, اصبحت 20</span> <span dir="rtl">بتكوين, وكذلك بنفس الشي
بين فراس وحمد غيرنا القيمه من 100 إلى 50. لو قمنا بطباعة محتوى
الـ</span>Hash <span dir="rtl">الخاص بالـ</span> Genesis Block
<span dir="rtl">مره اخرى سيكون الناتج</span> 729499183<span dir="rtl">-
مختلف عن القيمه السابقه, وهو دليل على تغير الـ</span>Digital ID
<span dir="rtl">الخاص بهذا الـ</span>Block<span dir="rtl">. وهذا مهم
جدا, لأنه عندما ننشئ الـ</span>Block <span dir="rtl">رقم 2 في
السلسله, سيحتاج الـ</span>Hash <span dir="rtl">الخاص
بالـ</span>Block <span dir="rtl">السابق (الـ</span>Genesis
Block<span dir="rtl">) ويحتاج ايضا نوع خاص فيه من
الـ</span>Transactions<span dir="rtl">. في الخطوه التاليه نوضح
بالـ</span>Code <span dir="rtl">كيف نترجم هذا الكلام بلغة</span>
Java<span dir="rtl">.</span>

String \[\] block2Transactions = {"Ali sent 5 bitcoin to Sami", "Sultan
received 2 bitcoin from Ahmed"};

Block block2 = **new** Block(genesisBlock.getBlockHash(),
block2Transactions);

*blockchain*.add(block2); <span dir="rtl"> </span>

<span dir="rtl">العمليات اللتي تمت في الـ</span>Block
<span dir="rtl">رقم 2 هي كالتالي: علي ارسل 5 بيتكوين لسامي, و سلطان
استقبل 2 بتكوين من أحمد, وهذي هيا الـ</span>Transactions
<span dir="rtl">الخاصه بالـ</span>Block <span dir="rtl">رقم 2 في هذا
الـ</span>Blockchain<span dir="rtl">. الأن بنفس الطريقه نقوم بطباعة
الـ</span>Digital ID <span dir="rtl">الخاص بالـ</span>Block
<span dir="rtl">رقم 2:</span>

System.*out*.println("Hash of block 2:");

System.*out*.println(*blockchain*.get(1).getBlockHash());

<span dir="rtl">نلاحظ بأن الـ</span>Digital ID <span dir="rtl">الخاص
بالـ</span>Block <span dir="rtl">رقم 2 هو</span>
1908707073<span dir="rtl">.الجميل في الموضوع هو لو قمنا فقط بتغيير محتوى
العمليات (الـ</span>Transactions<span dir="rtl">) في الـ</span>Block
<span dir="rtl">رقم 1 (</span>Genesis Block<span dir="rtl">) مثلا عوضا
ان يرسل سلطان لفراس 20 بتكوين, اصبحت 40 بتكوين, وقمنا بطباعة
الـ</span> Digital ID <span dir="rtl">الخاص بالـ</span>Blocks
<span dir="rtl">رقم 1 و 2 معا, ماذا سيحدث؟</span>

String\[\] genesisTransactions = {"Sultan sent Feras 40 bitcoin","Feras
sent 50 bitcoins to Hamad"};

Block genesisBlock = **new** Block(0, genesisTransactions);

*blockchain*.add(genesisBlock);

String\[\] block2Transactions = {"Ali sent 5 bitcoin to Sami", "Sultan
recived 2 bitcoin from Ahmed"};

Block block2 = **new** Block(genesisBlock.getBlockHash(),
block2Transactions); *blockchain*.add(block2);

System.*out*.println("Hash of genesis block:");
System.*out*.println(*blockchain*.get(0).getBlockHash());

System.*out*.println("Hash of block 2:");

System.*out*.println(*blockchain*.get(1).getBlockHash());

<span dir="rtl">سنلاحظ بأن الـ</span>Hash <span dir="rtl">لكل
الـ</span>Blocks <span dir="rtl">في هذا الـ</span>Blockchain
<span dir="rtl">تغيرت تماما بسبب التغيير البسيط الحاصل في
الـ</span>Genesis Block <span dir="rtl">:</span>

Hash of genesis block:

\-471333745

Hash of block 2:

\-2128094785

<span dir="rtl">وهذا هو الأساس المبني عليه تقينة
الـ</span>Blockchain<span dir="rtl">, بأن أي تغيير على</span> Block
<span dir="rtl">سيتم التأثير على جميع الـ</span>Blocks
<span dir="rtl">في هذه السلسله. مثلا لو عملنا</span> Block
<span dir="rtl">رقم 3 مع الأخذ بعين الإعتبار أن الـ</span>Hash
<span dir="rtl">السابق هو الـ</span>Hash <span dir="rtl">الخاص
بالـ</span>Block <span dir="rtl">رقم 2 والـ</span>Transactions
<span dir="rtl">الخاصه بهذا الـ</span>Block <span dir="rtl">(رقم 3) هي
فقط "أحمد ارسل 100 بتكوين لأمه"</span> <span dir="rtl">وقمنا بنفس
العمليه السابقه (نغير محتويات الـ</span>Genesis Block
<span dir="rtl">فقط) سنلاحظ التغيير يأثر على جميع الـ</span>Blocks
<span dir="rtl">(رقم 2 و 3) المرتبطه مع بعض في
الـ</span>Blockchain<span dir="rtl">.</span>

**void** buildBlockchain(ArrayList\<Block\> blockchain){

String\[\] genesisTransactions = { "Sultan sent Feras 40 bitcoin",

"Feras sent 50 bitcoins to Hamad" };

Block genesisBlock = **new** Block(0, genesisTransactions);

blockchain.add(genesisBlock);

String\[\] block2Transactions = { "Ali sent 5 bitcoin to Sami",

"Sultan recived 2 bitcoin from Ahmed" };

Block block2 = **new**
Block(genesisBlock.getBlockHash(),block2Transactions);

blockchain.add(block2);

String\[\] block3Transactions = { "Ahamed sent 100 bitcoin to his mom"
};

Block block3 = **new** Block(block2.getBlockHash(), block3Transactions);

blockchain.add(block3);

System.*out*.println("Hash of genesis block:");

System.*out*.println(blockchain.get(0).getBlockHash());

System.*out*.println("Hash of block 2:");

System.*out*.println(blockchain.get(1).getBlockHash());

System.*out*.println("Hash of block 3:");

System.*out*.println(blockchain.get(2).getBlockHash());

}

<span dir="rtl">أخيرا, الـ</span>Hashing Algorithms <span dir="rtl">صعب
جدا كسرها, بمعنى يصعب على المخترق ان يتعرف على طريقة عمل الخوارزميه
اللتي تنتج الـ</span>Hash <span dir="rtl">وبالتالي يستطيع ان يخمن
الأجوبه الصحيحه لكل</span> Block<span dir="rtl">. وبالتالي كلما زاد
عدد الـ</span>Blocks <span dir="rtl">في السلسله
(</span>chain<span dir="rtl">) كلما زادت عملية التعقيد لكسر
الـ</span>Hashes <span dir="rtl">المرتبطه مع بعضها البعض, لأن كما
ذكرت سابقا بان كل</span> Hash <span dir="rtl">مرتبط حسابيا
بالـ</span>Hash <span dir="rtl">اللذي قبله ولذلك اذا اردنا كسر
(</span>Crack<span dir="rtl">) الـ</span>Hash <span dir="rtl">الخاص
بالـ</span>Block <span dir="rtl">رقم 3 يلزمك ان تقوم بكسر
الـ</span>Hash <span dir="rtl">اللذي يعتمد (الـ</span>Hash
<span dir="rtl">الخاص برقم 2) ولكي تنجح بكسر الـ</span>Hash
<span dir="rtl">السابق يلزمك ان تعرف الـ</span>Hash
<span dir="rtl">السابق وهكذا. وبالتالي هذه العمليه اللتي تجعل من
تقنية الـ</span>Blockchain <span dir="rtl">اكثر امان لتداول عملة
الـ</span>Bitcoin <span dir="rtl">وعليه لو أن شخص في شبكة
الـ</span>Blockchain <span dir="rtl">عمل تغيير في سجلاته
(</span>Transactions<span dir="rtl">) الجميع في الشبكه سيعرفون انه عمل
تغيير في الـ</span>Transactions <span dir="rtl">لأن الـ</span>Hash
<span dir="rtl">القديم لن يكون مطابق للـ</span>Hash
<span dir="rtl">الجديد, فبالتالي بناء على البروتوكول المتبع في
الـ</span>Bitcoin <span dir="rtl">يجب التحقق من صحة الـ</span>Hash
<span dir="rtl">الجديد هل هو عمليه صحيحه تمت ام لا, وعليه ندخل في مفهوم
الـ</span>Bitcoin mining <span dir="rtl">ومفهوم الـ</span>Ledger
<span dir="rtl">(مفهوم المحفظه الماليه) الخاصه بتعاملات
الـ</span>Bitcoin<span dir="rtl">. سنحاول ان نفرد درس خاص بهذا
الموضوع مستقبلا أن شاء الله.</span> <span dir="rtl"> </span>
