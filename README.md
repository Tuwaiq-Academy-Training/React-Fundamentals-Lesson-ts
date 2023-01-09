# React-Fundamentals-Lesson-ts

# مقدمة في React

# سوف نتعلم في هذا الدرس :
* التعرف على اساسيات رياكت والتعامل معه 


تعتبر React مكتبة تستخدم لكتابة او تطوير واجهات المستخدم، ونعني بواجهات المستخدم هنا هو كل ما يتفاعل معه المستخدم في الصفحة. يوجد العديد من المكتبات و frameworks التي تساعدنا على كتابة واجهات المستخدم ايضا لكن تمتلك React عدد من المميزات أحدها اعتماد React على مفهوم Components واعادة استخدامها. بحيث تقوم React بتقسيم الواجهة الى أجزاء Components لتمكننا من إعادة استخدام هذه الأجزاء في أي صفحة أخرى.


**مثال**

![](https://paper-attachments.dropbox.com/s_AF539446F48191BDC6D15DF619AB61846567F12988213478724D17088942E1BE_1627564882791_image.png)




**أمثلة على صفحات تستخدم React:** 
Twitter

![](https://paper-attachments.dropbox.com/s_AF539446F48191BDC6D15DF619AB61846567F12988213478724D17088942E1BE_1627564997049_Screen+Shot+1442-12-19+at+4.23.13+PM.png)




instagram 

![](https://paper-attachments.dropbox.com/s_AF539446F48191BDC6D15DF619AB61846567F12988213478724D17088942E1BE_1627565081413_Screen+Shot+1442-12-19+at+4.24.37+PM.png)


نلاحظ هنا عدد من الصّور، و بالحقيقة بالرغم من وجود عدد منهم الّا انهم مجرد Component واحد لكن تمت اعادة استخدامه من خلال تغيير البيانات التي سيعرضها فقط. 

Virtual DOM 
 
 احد أهم اسباب استخدامنا React هو طريقة تعامله مع DOM وهو اختصار Document Object Model
 وهو يعرض العناصر اللتي تمت كتابتها في واجهات المستخدم UI ملفات HTML.

وكما هو موضح بالصوره يوجد لدينا شجرة DOM 

![DOM](https://paper-attachments.dropbox.com/s_DAF8495B9527B6244380D0BECA61ECAFD00DB0357A206D274592DE9435EE1DEE_1648376710649_DOM-01.png)


 
 
 بحيث في كل مره يتم عمل تغيير على ملف واجهات المستخدم (HTML) يقوم DOM بعمل تحديث على جميع العناصر وهذا قد يؤثر على سرعة العمل للتطبيق في حال كان لديك الكثير من العناصر. لنقل مثلا ان لديك اكثر من خمسين عنصر  في ملف HTML فهذا يعني انه سوف يقوم بتحديثها جميعها وهذا يؤثر في اداء التطبيق.



  # مفهوم virtual dom

 بعد رؤية المفهوم الحقيقي لDOM وكيف انه قد يؤثر في عمل التطبيق جاء هنا مفهوم virtual dom
 وهو بعكس الDOM الحقيقي فإنه لايقوم بتحديث كامل للعناصر فقط يقوم بتحديث العنصر الذي احدثنا عليه التغيير وبهذا قمنا بتسريع عمل التطبيق.
  لكن هذا لايعني انه تم عمل DOM جديد وحذف الDOM الحقيقي بل تم عمل نسخة منه ومقارنة التغيير الذي حدث معه ومن ثم تطبيقها على العنصر 

![](https://paper-attachments.dropbox.com/s_DAF8495B9527B6244380D0BECA61ECAFD00DB0357A206D274592DE9435EE1DEE_1648376894171_DOM-02.png)


 
 
 
 
 



  






# ابدأ مع React

للبدء مع React دعونا أولا ننشئ مجلّد بداخله ملف html من ثمّ التطبيق على كيفيّة البدء باستخدام React كالتالي.


![](https://paper-attachments.dropbox.com/s_AF539446F48191BDC6D15DF619AB61846567F12988213478724D17088942E1BE_1627565965166_Screen+Shot+1442-12-19+at+4.39.21+PM.png)


لنقم الآن بتجهيز الملف كملف html كالتالي. 

    <html>
        <head>
        </head>
        <body> 
        </body>
    </html>
![](https://paper-attachments.dropbox.com/s_AF539446F48191BDC6D15DF619AB61846567F12988213478724D17088942E1BE_1627566315848_Screen+Shot+1442-12-19+at+4.45.10+PM.png)


بهذا الشكل قمنا بتجهيز الملف، المتبقي هو ان نقوم باضافة مكتبة React للتعامل معها من خلال الذهاب الى موقع React عبر الرابط ( https://reactjs.org/ )  من ثمّ نسخ CDN الخاص في React و ReactDOM.

CDN 

    <script crossorigin src="https://unpkg.com/react@17/umd/react.production.min.js"></script>
    
    <script crossorigin src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script>


**مثال**

    <html>
        <head>
            <script crossorigin src="https://unpkg.com/react@17/umd/react.production.min.js"></script>
            <script crossorigin src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script>
        </head>
        <body> 
        </body>
    </html>
    
![](https://paper-attachments.dropbox.com/s_AF539446F48191BDC6D15DF619AB61846567F12988213478724D17088942E1BE_1627566668395_Screen+Shot+1442-12-19+at+4.51.04+PM.png)


بهذا الشكل اصبحنا جاهزين للتطبيق. 



React Project Folders Structure

![](https://paper-attachments.dropbox.com/s_4E006B11E5DBB82EDCA48627D3C762AF436F0810CB03CE9027FA25A16CFDB33C_1648456556250_Screen+Shot+1443-08-25+at+11.35.13+AM.png)

- مجلد node_modules يحتوي على كل المجلدات التي تحوي التبعيات المعتمد عليها مشروع الرياكت.
- مجلد  public يحتوي على ملف الـHTML الاساسي للمشروع.
- في مجلد src ننشئ مجلد باسم Components  بداخله ننشئ أي مكوّن نحتاجه في مشروع الرياكت.
- في ملف .gitignore نضع معلومات الملفات التي لا نريد من git تتبعها.
- ملف package-lock.json يحتوي على تفاصيل كل الحزم والمكتبات التي تم تنزيلها في المشروع، كما يمكن ادارتها في هذا الملف.
- ملف package.json يحتوي على كل الحُزم والمكتبات التي تم تنزيلها في المشروع.
- في ملف README.md نستطيع كتابة وصف المشروع.

***عناصر React***


العناصر في React هي عبارة عن كائن object يمثل وصف جزء من UI حيث إن العنصر يمثل أصغر وحدة في بناء واجهة المستخدم في React ويمكننا انشاء العنصر باستخدام الدّالة createElement.

تعريف دالّة createElement

    React.createElement(type, properties, [...children])

نلاحظ أن دالة `createElement` تستقبل ثلاث مدخلات المدخل الأول `type` يمثل نوع العنصر أما المدخل الثاني `properties` يمثل خصائص العنصر مثل `id` وغيرها، أما المدخل الثالث ومابعده `children` يمثل محتوى العنصر مثل النّص ان كان يحتوي العنصر على نص او عنصر آخر.

**مثال**

    const element = React.createElement("h1", null, "Welcome to React");

نلاحظ أننا قمنا بتمرير ثلاث قيم لدالة `createElement` حيث أن قيمة المدخل الأول `h1` تمثل نوع العنصر، بينما قيمة المدخل الثاني `null` تمثل خصائص العنصر وآخر قيمة المدخل الثالث `Welcome to React` تمثل محتوى العنصر.


إضافة خصائص لعنصر React
لنفترض أننا نريد إضافة خاصية لعنصر React، نقوم بذلك عن طريق كتابة اسم الخاصية ومن ثم قيمتها داخل object الخصائص كما هو موضح في المثال التالي:

    const element = React.createElement("a", {
      href: "https://reactjs.org"
    }, "Hello React");

في المثال السابق قمنا بإضافة `href` إلى العنصر وذلك عن طريق كتابة اسم الخاصية وقيمته في object الخصائص.



إنشاء عنصر React يحتوي على عناصر React أخرى
كما ذكرنا سابقًا أن المدخل الثالث لدالة `createElement` التي بداخل `React` تمثل المحتوى لهذا العنصر لذلك من الممكن أن يكون محتوى عنصر ماهو عبارة عن عنصر آخر لتوضيح هذهِ الفكرة نلاحظ المثال التالي:

    const elementOne = React.createElement("h1", null, "Welcome to React");
    const elementTwo = React.createElement("p", null, "React is a JavaScript library for building user interfaces")
    const element = React.createElement("div", null, elementOne, elementTwo);

في المثال السابق في السطر الأول قمنا بإنشاء عنصر `elementOne` أما في السطر 2 قمنا بإنشاء عنصر آخر `elementTwo` في السطر 3 قمنا بإنشاء عنصر ووضعنا محتواه عنصر `childElementOne` و `childElementTwo`.


# إنشاء عنصر React بإستخدام JSX

تتشابه طريقة إنشاء عنصر React بإستخدام JSX لطريقة إنشاء عنصر في HTML. لتوضيح هذه الفكرة نلاحظ السطر التالي:

    const element = <h1>Welcome to React</h1>;

في السطر السابق قمنا بإنشاء عنصر React من نوع `h1` محتواه هو `Welcome to React`.


# إضافة خصائص لعنصر React باستخدام JSX

طريقة إضافة خاصية إلى عنصر React باستخدام JSX هي مشابهة لطريقة إضافة خاصية إلى عنصر في HTML ولتوضيح هذهِ الفكرة نلاحظ السطر التالي:

    const element = <a href="https://reactjs.org">Hello React</a>;

في المثال السابق قمنا بإضافة `href` إلى العنصر وذلك عن طريق كتابة اسم الخاصية وقيمته داخل start tag.



# إنشاء عنصر React يحتوي على عناصر React باستخدام JSX
طريقة إنشاء عنصر React يحتوي على عنصر React آخر هي مشابهة لطريقة إنشاء عنصر داخل عنصر في HTML ولتوضيح هذهِ الفكرة نلاحظ المثال التالي:

    const element = <div>
                        <h1>Welcome to React</h1>
                        <p>React is a JavaScript library for building user interfaces</p>
                    </div>;

في المثال السابق قمنا بإنشاء عنصر React يحتوي على عنصرين آخرين. 
ملاحظة: في JSX إذا كان لديك أكثر من عنصر يجب تضمينهم داخل عنصر واحد.



# تعبيرات JSX المتغيرات
يمكنك كتابة متغير أو ثابت داخل JSX وذلك عن طريق تضمينه داخل القوسين `{}` كما هو موضح في المثال التالي:

    const name = "Omar";
    const element = <h1> Hello my name is {name}</h1>;

لاحظ في السطر الثاني قمنا بتضمين الثابت `name` داخل JSX. المصدر



#تعبيرات JSX عامل الشرط الثلاثي
يمكنك أيضًا كتابة عامل الشرط الثلاثي بداخل JSX وذلك عن طريق تضمينه داخل `{}` كما في السطر الثاني:

    const age = 17;
    const message = <p>{age >= 18 ? "You can drive" : "You cannot drive"}</p>

في السطر الثاني ستكون قيمة محتوى عنصر React هي `You cannot drive` وذلك لأن نتيجة الشرط هي `false`.



# تعبيرات JSX دوال المصفوفات
يمكنك أيضًا كتابة دوال المصفوفات داخل JSX وذلك عن طريق تضمينها داخل القوسين `{}` كما في المثال التالي:

    const colors = ["red", "green", "blue"];
    const colorsList = <ul> {colors.map( (color, index) => <li key={index}>{color}</li> )} </ul>

في السطر الثاني ستكون نتيجة المصفوفة الجديدة عبارة عن عناصر React نوعها `li` ومن ثم سيتم إدخال العناصر داخل العنصر `ul`.
ملاحظة: كل عنصر في المصفوفة يجب أن تضاف مع قيمة فريدة من نوعها تسند لخاصية `key` لأجل أن يتم عرض وصف UI بشكل مناسب لذلك استخدمنا index العنصر كقيمة فريدة.



# إدخال عنصر React إلى DOM
لإدخال عنصر React داخل DOM يتم استدعاء الدالة `render` وتقوم هذهِ الدالة بوضع عنصر React داخل الحاوية -الحاوية تكون موجودة في DOM - وهي المكان المراد إدخال عنصر React داخلها، توضح الصيغة التالية كيفية القيام بذلك:

    ReactDOM.render(element, container)

نلاحظ دالة `render` تستقبل مدخلين حيث أن المدخل الأول `element` يمثل العنصر أما المدخل الثاني يمثل `container` -حيث أن هذا `container` موجود DOM- الذي سيحتضن `element`.
نلاحظ تطبيقها في المثال التالي:

    const container = document.getElementById("root");
    ReactDOM.render(element, container);

نلاحظ أن الدالة `render` تستقبل مدخلين حيث أن المدخل الأول `element` يمثل عنصر React أما المدخل الثاني يمثل الحاوية `container` الذي سيحتضن `element`.



بهذا الشكل اصبحنا جاهزين للتطبيق
مفهوم المكونات Component

 
