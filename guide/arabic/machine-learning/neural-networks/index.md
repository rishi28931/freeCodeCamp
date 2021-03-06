---
title: Neural Networks
localeTitle: الشبكات العصبية
---
## الشبكات العصبية

![تغذية الشبكة العصبية إلى الأمام](http://ufldl.stanford.edu/tutorial/images/SingleNeuron.png)

الشبكة العصبية الاصطناعية هي نظام الحوسبة. هم مثل الشبكات العصبية البيولوجية التي تشكل أدمغة الحيوانات. لتدريب الشبكة العصبية ، نحتاج إلى متجه مدخلات وناقل إخراج مناظرة. يعمل التدريب عن طريق تقليل مصطلح الخطأ. يمكن أن يكون هذا الخطأ الفرق التربيعية بين الإخراج المتوقع والإخراج الأصلي.

المبدأ الأساسي الذي يكمن وراء النجاح الملحوظ للشبكات العصبية هو "نظرية التقريب العالمي". وقد ثبت رياضيا أن الشبكات العصبية هي آلات تقريب عالمية قادرة على تقريب أي دالة رياضية بين المدخلات والمخرجات.

أصبحت الشبكات العصبية في البداية شائعة في ثمانينيات القرن العشرين ، لكن القيود في القوة الحسابية منعت قبولها على نطاق واسع حتى العقد الماضي. تسمح الابتكارات في حجم وحدة المعالجة المركزية وقوتها بتطبيق الشبكات العصبية على نطاق واسع ، على الرغم من أن نماذج التعلم الآلي الأخرى لا تزال تفوق الشبكات العصبية من حيث الكفاءة.

العنصر الأساسي في الشبكة العصبية هو العصبون. هو إدخال هو ناقل ، ويقول `x` ، وخرجه هو متغير قيمة حقيقية ، ويقول `y` . وهكذا ، يمكننا أن نستنتج أن العصبون يعمل كخريطة بين المتجه `x` وعدد حقيقي `y` .

تقوم الشبكات العصبية بالانحدار التكراري عبر طبقات متعددة ، مما يؤدي إلى نموذج تنبؤ أكثر دقة. يحسب عقدة واحدة في شبكة عصبية نفس الوظيفة بالضبط مثل [الانحدار اللوجستي](../logistic-regression/index.md) . كل هذه الطبقات ، بخلاف المدخلات والمخرجات ، مخفية ، أي أن السمات المحددة التي تمثلها هذه الطبقات لا يتم اختيارها أو تعديلها بواسطة المبرمج.

![أربع طبقات الشبكة العصبية](http://cs231n.github.io/assets/nn1/neural_net2.jpeg)

في أي طبقة ، تأخذ كل عقدة جميع القيم المخزنة في الطبقة السابقة كمدخل وتقوم بتوقعات عليها استنادًا إلى تحليل الانحدار اللوجستي. تكمن قوة الشبكات العصبية في قدرتها على "اكتشاف" الأنماط والسمات غير المرئية من قبل المبرمجين. وكما ذكرنا سابقًا ، فإن الطبقات الوسطى "مخفية" ، بمعنى أن الأوزان الممنوحة للتحولات يتم تحديدها حصريًا بتدريب الخوارزمية.

يتم استخدام الشبكات العصبية في مجموعة متنوعة من المهام. وتشمل هذه الرؤية الكمبيوتر ، والتعرف على الكلام ، والترجمة ، وتصفية الشبكات الاجتماعية ، ولعب ألعاب الفيديو ، والتشخيص الطبي من بين أمور أخرى.

### تصور

هناك أداة رائعة تساعدك على فهم فكرة الشبكات العصبية بدون أي رياضيات صلبة: [TensorFlow Playground](http://playground.tensorflow.org) ، وهو تطبيق ويب يتيح لك اللعب باستخدام شبكة عصبية حقيقية تعمل في متصفحك ، ثم النقر على أزرار وتعديل المعلمات لمعرفة كيفية عملها.

### حل المشاكل باستخدام الشبكات العصبية

*   تصنيف
*   تجمع
*   انحسار
*   إكتشاف عيب خلقي
*   قواعد الرابطة
*   تعزيز التعلم
*   التنبؤ الهيكلي
*   هندسة الميزة
*   تعلم مميز
*   تعلم لترتيب
*   التحفيز النحوي
*   التنبؤ بالطقس
*   توليد الصور

### نظم الشبكات العصبية المشتركة

تندرج الشبكات العصبية الأكثر استخدامًا اليوم في فئة [التعلم العميق](https://github.com/freeCodeCamp/guides/blob/master/src/pages/machine-learning/deep-learning/index.md) . التعلّم العميق هو عملية ربط طبقات متعددة من العصبونات للسماح لشبكة ما بإنشاء تصميمات مجردة بشكل متزايد بين نواقل المدخلات والمخرجات. ستستخدم الشبكات العصبية العميقة بشكلٍ عام [دعامات النسخ الخلفية من](https://github.com/freeCodeCamp/guides/blob/master/src/pages/machine-learning/backpropagation/index.md) أجل الوصول إلى أكثر الخرائط دقة.

الشكل الثاني الأكثر شيوعًا للشبكات العصبية هو nueroevolution. في هذا النظام يتم إنشاء شبكات عصبية متعددة بشكل عشوائي كتخمينات أولية. ثم يتم استخدام أجيال متعددة من دمج معظم الشبكات الدقيقة والتباديل العشوائي للالتقاء على رسم خرائط أكثر دقة.

### أنواع الشبكات العصبية

*   الشبكة العصبية المتكررة (RNN)
*   الذاكرة طويلة المدى (LSTM) ، وهو نوع من RNN
*   الشبكة العصبية التلافيفية (CNN)

### معلومات اكثر:

*   [الشبكات العصبية - ويكيبيديا](https://en.wikipedia.org/wiki/Artificial_neural_network#Components_of_an_artificial_neural_network)
*   [طبيعة دانيال شيفمان من المدونة](http://natureofcode.com/book/chapter-10-neural-networks/)
*   [جامعة ستانفورد ، الشبكات العصبية متعددة الطبقات](http://ufldl.stanford.edu/tutorial/supervised/MultiLayerNeuralNetworks/)
*   [3Blue1Brown ، قناة Youtube مع محتوى الشبكة العصبية](https://youtu.be/aircAruvnKk)
*   [Siraj Raval ، يوتيوب CHannel مع محتوى الشبكة العصبية](https://youtu.be/h3l4qz76JhQ)
*   [Neuroevolution - ويكيبيديا](https://en.wikipedia.org/wiki/Neuroevolution)