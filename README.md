# pyarabic
A specific *Arabic language* library for **Python**, provides basic functions to manipulate Arabic letters and text, like detecting Arabic letters, Arabic letters groups and characteristics, remove diacritics etc.

مكتبة برمجية للغة العربية بلغة بيثون، توفر دوالا للتحكم في الحروف والنصوص، مثلا تحديد نوع الحرف، حذف الحركات، مقارنة التشكيل.


  Developpers:  Taha Zerrouki: http://tahadz.com
    taha dot zerrouki at gmail dot com

Features |   value
---------|---------------------------------------------------------------------------------
Authors  | Taha Zerrouki: http://tahadz.com,  taha dot zerrouki at gmail dot com
Release  | 0.6.2
License  |[GPL](https://github.com/linuxscout/pyarabic/master/LICENSE)
Tracker  |[linuxscout/pyarabic/Issues](https://github.com/linuxscout/pyarabic/issues)
Website  |[https://pypi.python.org/pypi/pyarabic](https://pypi.python.org/pypi/pyarabic)
Doc  |[package Documentaion](http://pythonhosted.org/pyarabic/)
Source  |[Github](http://github.com/linuxscout/pyarabic)
Download  |[pypi.python.org](https://pypi.python.org/pypi/pyarabic)
Feedbacks  |[Comments](https://github.com/linuxscout/pyarabic/issues)
Accounts  |[@Twitter](https://twitter.com/linuxscout)  [@Sourceforge](http://sourceforge.net/projects/pyarabic/)



## Citation
If you would cite it in academic work, can you use this citation
```
T. Zerrouki‏, Pyarabic, An Arabic language library for Python,
  https://pypi.python.org/pypi/pyarabic/, 2010
```
or in bibtex format

```bibtex
@misc{zerrouki2012pyarabic,
  title={pyarabic, An Arabic language library for Python},
  author={Zerrouki, Taha},
  url={https://pypi.python.org/pypi/pyarabic,
  year={2010}
}
```


## مزايا
* تصنيف الحروف
* تفريق النص إلى وحدات
* حذف الحركات:( كل الحركات، الحركات عدا الشدة، حذف الشدة، حذف التطويل، حذف الحركة الأخيرة)
* فصل الحركات عن النصوص وإدماجها
* اختزال التشكيل
* قياس التماثل بين كلمتين ( في الحركات جزئيا وكليا، التماثل مع وزن)
* تنميط الحروف ( توحيد التراكيب مثل لام الألف، والهمزات)
* تحويل الأعداد إلى كلمات
* استخلاص العبارات العددية من النص
* تشكيل أولي للعبارات العددية
* قلب النصوص العربية للأنظمة التي لا تدعم تشبيك الحروف

## Features
* Arabic letters classification
* Text tokenization
* Strip Harakat ( all, except Shadda, tatweel, last_haraka)
* Sperate and  join Letters and Harakat
* Reduce tashkeel
* Mesure tashkeel similarity ( Harakats, fully or partially vocalized, similarity with a template)
* Letters normalization ( Ligatures and Hamza)
* Numbers to words
* Extract numerical phrases
* Pre-vocalization of numerical phrases
* Unshiping texts


Applications
====
* Arabic text processing

Installation
=====
```
pip install pyarabic
```    
    
Usage
=====
```python
import pyarabic.araby as araby
import pyarabic.number as number
```




Package Documentation
=====
[https://pythonhosted.org/PyArabic/](https://pythonhosted.org/PyArabic/)

Files
=====
* file/directory    category    description 
 * araby.py: arabic routins.
 * named.py: handle named enteties recognation.
 * unshape.py: unshaping arabic text

# وصف
مكتبة بيثون للعربيةPyArabic  مكتبة برمجية تجمع في طياتها خصائص ووظائف يحتاجها المبرمج للتعامل مع النصوص العربية، وهي مستوحاة من مكتبة بي أتش بي العربية لصديقنا خالد الشمعة، التي تستهدف توفير مصدر مفتوح لكثير من وظائف النصوص العربية لاستعمالها في مجال النشر في الإنترنت.

#تعريف نص عربي
أفضل طريقة للتعامل مع النصوص العربية بلغة بيثون هو استخدام الترميز يونيكود، التي يدعمها بيثون دعما أصليا، لا حاجة فيه إلى مكتبات خارجية أو دوال خاصة، وقد يكون هذا أهمّ ما دفعني لاختيار لغة بيثون، إذ يكفي أن تسبق النص بحرف يو u  لتدع بيثون يريحك من عناء التفكير وبرمجة النصوص، ويعامل معها بشفافية عالية.

تعريف نص عربي بترميز يونيكود

```python
text = u'الإسلام ديننا'
```

اختيار ترميز ملف المتن.
```
﻿#!/usr/bin/env python
# -*- coding: utf-8 -*-
```

عرض النص العربي في المخرج
```
print text.encode('utf8')
```

اسم المكتبة pyarabic
فيها العديد من الوظائف المجمعة في وحدات:

فيها العديد من الوظائف المجمعة في وحدات:
* وحدة : araby.py  وفيها الثوابت كالحروف وأسمائها ومجموعاتها والوظائف العامة كحذف الحركات وحذف التطويل ومقارنة التشكيل بين الكلمات، وضبط  علامات الترقيم.
* وحدة الأعداد number.py : وفيها وظائف تحويل الأعداد إلى كلمات والكلمات إلى أعداد، كشف ألفاظ الأعداد في النص، وتشكيلها.
* وحدة المسميات : named.py وفيها وظائف لكشف الأسماء والمسميات في النص.


### وحدة الوظائف العامة araby
يمكن استدعاؤها بالأمر 
```python
Import pyarabic.araby as araby
```

وسنستعمل الاختصار araby  فيما بعد
الثوابت العامة في مكتبة عربي:
تضم الحروف العربية  ومجموعاتها المختلفة وبعض الأنماط المستخدمة لاحقا في وظائف مختلفة
1- الحروف العربية الأساسية مع تسميات لاتينية لاستعمالها في البرمجة

The arabic chars contains all arabic letters, a sub class of unicode,

```python
COMMA            = u'\u060C'
SEMICOLON        = u'\u061B'
QUESTION         = u'\u061F'
HAMZA            = u'\u0621'
ALEF_MADDA       = u'\u0622'
ALEF_HAMZA_ABOVE = u'\u0623'
```
المزيد في ملف araby.py

تضم مجموعة الحروف العربية الحروف الأساسية، والحركات والأرقام، وعلامات الترقيم، وبعض الحروف الخاصة كالألف الخنجرية والياء الصغيرة، و لامات الألف بأشكالها.
####مجموعات الأحرف: 
ويمكن تقسيم الحروف في مجموعات وتصنيفات نستعملها فيما بعد في الوظائف المختلفة

الاسم العربي | وصف المجموعة | عناصرها
--------|--------------|------------
الحروف | مجموعة الحروف العربية دون حركات | LETTERS = u'ابتةثجحخدذرزسشصضطظعغفقكلمنهويءآأؤإئ' 
التشكيل  | مجموعة الحركات مع الشدة مدرجة  | TASHKEEL =(FATHATAN, DAMMATAN, KASRATAN, FATHA,DAMMA,KASRA, SUKUN,   SHADDA)
الحركات | مجموعة الحركات دون الشدة مدرجة | HARAKAT =(  FATHATAN,   DAMMATAN,   KASRATAN,  FATHA,  DAMMA,  KASRA, SUKUN);
الحركات القصيرة | الحركات القصيرة دون تنوين | SHORTHARAKAT =( FATHA,  DAMMA,  KASRA, SUKUN);
التنوين | حركات التنوين | TANWIN =(FATHATAN,  DAMMATAN,   KASRATAN);
المركبات | لامات الألف في أشكالها المختلفة | LIGUATURES = (u'ﻻ', u'ﻷ', u'ﻹ', u'ﻵ') 
الهمزات | الهمزة في أشكالها المختلفة | HAMZAT = (u'ء', u'ؤ', u'ئ', u'ٔ', u'ٕ', u'إ', u'أ') 
الألفات | الألف في أشكالها المختلفة | ALEFAT = (u'ا', u'آ', u'أ', u'إ', u'ٱ', u'ى', u'ٰ') 
حروف العلة | الياء والواو والألف | WEAK = (u'ا', u'و', u'ي', u'ى') 
الياءات | ما يرسم مثل الياء، الصغيرة منها، والألف المقصورة والهمزة على النبرة | YEHLIKE = (u'ي', u'ئ', u'ى', u'ۦ') 
الواوات | ما يرسم مثل الواو | WAWLIKE = (u'و', u'ؤ', u'ۥ') 
التاءات | التاء المربوطة والمفتوحة | TEHLIKE = (u'ت', u'ة') 
الحروف الصغيرة | الألف والياء والواو الصغار | SMALL = (u'ٰ', u'ۥ', u'ۦ') 
الحروف القمرية | الحروف القمرية | MOON = (u'ء', u'آ', u'أ', u'إ', u'ا', u'ب', u'ج', u'ح', u'خ', ... 
الحروف الشمسية | الحروف القمرية | SUN = (u'ت', u'ث', u'د', u'ذ', u'ر', u'ز', u'س', u'ش', u'ص', u... 
ترتيب الحروف العربية | يعطي لكل حرف عربي رقما ترتيبيا فالألف واحد والباء اثنان والهمزة 29. | AlphabeticOrder = {u'ء': 29, u'آ': 29, u'أ': 29, u'ؤ': 29, u'إ... 
أسماء الحروف | يعطي كل حرف اسمه العربي | NAMES = {u'ء': u'همزة', u'آ': u'ألف ممدودة', u'أ': u'همزة على ... 


#### الوظائف- الدوال

##### أهم الوظائف

وصف الدالة  |الدالة
------|------------
حذف الحركات كلها بما فيها الشدة|strip_tashkeel(text)
حذف الحركات كلها ماعدا الشدة|strip_harakat(text)
حذف الحركة الأخيرة|strip_lastharaka(text)
حذف التطويل| strip_tatweel(text)
تنميط أشكال الهمزة المختلفة | normalize_hamza(text)
تفريق كلمات النص |tokenize(text)


* حذف الحركات

 * حذف كل الحركات عدا الشدة

Strip Harakat from arabic word except Shadda. The striped marks are :
Example:

```python
>>> text = u"الْعَرَبِيّةُ"
>>> strip_harakat(text)
>>> العربيّة
```
 * حذف الحركات بما فيها الشدة

Strip vowels from a text, include Shadda. The striped marks are :

```python
>>> text = u"الْعَرَبِيّةُ"
>>> strip_tashkeel(text)
العربية
```

 * حذف الحركة الأخيرة فقط:
 قد تكون هي الحركة الإعرابية، لكن ليس في كل الحالات، مثلا يضربه، حركة الإعراب على الباء وليس على الهاء

Strip the last Haraka from arabic word except Shadda. The striped marks are :
```python
>>> text = u"الْعَرَبِيّةُ"
>>> strip_lastharaka(text)
الْعَرَبِيّة
```

 * اختزال التشكيل 
Reduce the Tashkeel, by deleting evident cases.

```python
>>> word = u"يُتَسََلَّمْنَ"
>>> reduced = araby.reduce_tashkeel(word)
>>> print reduced.encode('utf8')
يُتسلّمن
```

*  حذف التطويل أو الشدة

Strip tatweel or Shadda from a text.

```python
>>> text = u"العـــــربية"
>>> strip_tatweel(text)
العربية
>>> text = u"الشّمسيّة"
>>> strip_shadda(text)
 الشمسية
```
 
* تنميط الحروف المركبة والهمزة

بعض البرامج تعطي حروف متراكبة، توحيدها يرجعها إلى حروف بسيطة

Normalize Lam Alef ligatures into two letters (LAM and ALEF)
    LAM_ALEF, LAM_ALEF_HAMZA_ABOVE, LAM_ALEF_HAMZA_BELOW, LAM_ALEF_MADDA_ABOVE
```python
>>> text = u"لانها لالء الاسلام"
>>> normalize_ligature(text)
لانها لالئ الاسلام
```

 * توحيد الهمزة

Standardize the Hamzat into one form of hamza, replace Madda by hamza and alef. Replace the LamAlefs by simplified letters.

```python
>>> text = u"سئل أحد الأئمة"
>>> normalize_hamza(text)
 سءل ءحد الءءمة
```

* فصل الحركات والحروف

يمكن استخلاص الحروف والحركات في سلسلتين متوازيتين، بحيث يقابل كل حرف حركة محددة، إذا غابت الحركة رمزنا لها بتطويل

separate the letters from the vowels, in arabic word, if a letter hasn't a haraka, the not definited haraka is attributed. return ( letters, vowels)

```python
>>> araby.separate(text)
(u'\u0627\u0644\u0639\u0631\u0628\u064a\u0629', u'\u064e\u0652\u064e\u064e\u064e\u064e\u064f')
>>> letters, marks =araby.separate(text)
>>> print letters.encode('utf8')
العربية
>>> print marks.encode('utf8')
>>> for m in marks:
...     print araby.name(m)
فتحة
سكون
فتحة
فتحة
فتحة
فتحة
ضمة
```
يمكن دمج الحركات والحروف في كلمة واحدة، شرط أن يكون طول السلسلتين متساويا.
ينوب عن غياب الحركة حرف التطويل

joint the letters with the marks the length ot letters and marks must be equal return word

```python
>>> letters = u"العربية"
>>> marks   = u'\u064e\u0652\u064e\u064e\u064e\u064e\u064f'
>>> word = araby.joint(letters, marks)
>>> print word.encode('utf8')
اَلْعَرَبَيَةُ
```

* حساب التماثل

التماثل في الحركات بين كلمتين يون صحيحا 
إذا كان للكلمتين نفس الحروف، ونفس الحركات، ولو كانت الحركات ناقصة 

if the two words has the same letters and the same harakats, this fuction return True. The two words can be full vocalized, or partial vocalized

```python
>>> word1 = u"ضَربٌ"
>>> word2 = u"ضَرْبٌ"
>>> araby.vocalizedlike(word1, word2)
True
```

 * تماثل الوزن
تتماثل كلمة مع وزن إذا كانت الحروف تتطابق مع الوزن  والحركات مع الحركات، يمكن أن يكون التشكيل غير كامل

If the word1 is like a wazn (pattern), the letters must be equal, the wazn has FEH, AIN, LAM letters. this are as generic letters. The two words can be full vocalized, or partial vocalized

```python
>>> word1 = u"ضارب"
>>> wazn =  u"فَاعِل"
>>> araby.waznlike(word1, wazn)
True
```

 * تتماثل كلمتان في الشدة إذ كانت لهما نفس المكان، والحركات أيضا
وقد يكون التشكيل غير كامل

If the two words has the same letters and the same harakats, this fuction return True. The first word is partially vocalized, the second is fully if the partially contians a shadda, it must be at the same place in the fully

```python
>>> word1 = u"ردّ"
>>> word2=u"ردَّ"
>>> araby.shaddalike(word1, word2)
True
```

 * حساب التماثل في الحركات

نقيس التماثل في الحركات ، بحيث كل اختلاف ننقص 1
فنحصل على عدد سالب حسب عدد مرات الاختلاف

if the two words has the same letters and the same harakats, this function return True. The two words can be full vocalized, or partial vocalized

```python
>>> word1 = u"ضَربٌ"
>>> word2 = u"ضَرْبٌ"
>>> araby.vocalizedlike(word1, word2)
True
>>> word1 = u"ضَربٌ"
>>> word2 = u"ضَرْبٍ"
>>> araby.vocalized_similarity(word1, word2)
-1
```

*  تفريق النص

يمكن استعمال الدالة tokenize لتفريق النص إلى كلمات

Tokenize text into words.

```python 
>>> text = u"العربية لغة جميلة."
>>> tokens = araby.tokenize(text)
>>> print u"\n".join(tokens)
‎العربية
‎لغة
‎جميلة
.
```




#### وظائف الحروف
دوال الحروف وهي تعيد صواب إذا انتمى الحرف إلى المجموعة المطلوبة

وصف الدالة  |الدالة
------|------------
إذا كان الحرف المعطى سكونا يرجع صحيح | is_sukun(archar)
إذا كان الحرف المعطى شدة يرجع صحيح | is_shadda(archar)
إذا كان الحرف المعطى تطويلا يرجع صحيح | is_tatweel(archar)
إذا كان الحرف المعطى تنوينا يرجع صحيح | is_tanwin(archar)
إذا كان الحرف المعطى تشكيلا (حركة أو شدة) يرجع صحيح | is_tashkeel(archar)
إذا كان الحرف المعطى حركة يرجع صحيح | is_haraka(archar)
إذا كان الحرف المعطى حركة قصيرة يرجع صحيح | is_shortharaka(archar)
إذا كان الحرف المعطى لام ألف يرجع صحيح | is_ligature(archar)
إذا كان الحرف المعطى همزة يرجع صحيح | is_hamza(archar)
إذا كان الحرف المعطى ألفا يرجع صحيح | is_alef(archar)
إذا كان الحرف المعطى يماثل الياء في رسمه يرجع صحيح | is_yehlike(archar)
إذا كان الحرف المعطى يماثل الواو في رسمه يرجع صحيح | is_wawlike(archar)
إذا كان الحرف المعطى تاء مفتوحة أو مربوطة يرجع صحيح | is_teh(archar)
إذا كان الحرف المعطى حرفا صغيرا يرجع صحيح | is_small(archar)
إذا كان الحرف المعطى حرف علة يرجع صحيح | is_weak(archar)
إذا كان الحرف المعطى حرفا قمريا يرجع صحيح | is_moon(archar)
إذا كان الحرف المعطى حرفا شمسيا يرجع صحيح | is_sun(archar)

### مثال

في نطق الأسماء يتحوّل الحرف الشمسي بعد ال التعريف إلى حرف مشدد أي أنّ "الشمس" تنطق "أششمس"، 
```python
#!/usr/bin/python
# -*- coding=utf-8 -*-
import pyarabic.araby as araby
words=[u'الشمس', u'القمر', u'الرجل', u'بصل', u'البصل']
for word in words:
    if word.startswith(araby.ALEF+araby.LAM) and araby.isSun(word[2]):
        word=u''.join([araby.ALEF+word[2],word[2:]]);
    print word.encode('utf8');
```
في المثال، نعطي عددا من الكلمات لكتابة نطقها، بتحويل الحرف الشمسي بعد ال التعريف إلى حرف مكرر والنتيجة تكون 
```
اششمس
القمر
اررجل
بصل
البصل
```

# وظائف الأعداد والأرقام
number.py
توفر هذه المكتبة وظائف مثل : 
 * البحث عن مواضع العبارات العددية
 * تحويل الكلمات إلى أعداد، 
 * استخلاص العبارات العددية
 * تشكيلها
* تحويل الكلمات إلى أعداد
Convert arabic text into number, for example convert تسعة وعشرون = >29.

```python
>>> text2number(u"خمسمئة وثلاث وعشرون")
523
```

* تشكيل جملة كلمات عددية
Vocalize a number words clause

```python
>>> txt = u"خمسمئة وثلاثة وعشرين"
>>> wordlist = araby.tokenize(txt)
>>> vocalized =  vocalize_number(wordlist)
>>> print u" ".join(vocalized)
خَمْسمِئَة وَثَلاثَة وَعِشْرِينَ
>>>
```

* استخلاص العبارات العددية من جملة

Extract number words in a text.

```python
>>> extract_number_phrases(u"وجدت خمسمئة وثلاثة وعشرين دينارا فاشتريت ثلاثة عشر دفترا")
خمسمئة وثلاثة وعشرين
ثلاثة عشر
```

* استخلاص العبارات العددية مع سياقها

Extract number words in a text with context.

```python
>>> extract_number_context(u"وجدت خمسمئة وثلاثة وعشرين دينارا فاشتريت ثلاثة عشر دفترا")
‎وجدت، خمسمئة وثلاثة وعشرين، دينارا
‎فاشتريت، ثلاثة عشر ، دفتر
```

* استخلاص مواضع العبارات العددية

Detect number words in a text and return positions of each phrase.

```python
>>> txt = u"وجدت خمسمئة وثلاثة وعشرين دينارا فاشتريت ثلاثة عشر دفترا"
>>> wordlist = araby.tokenize(txt)
>>> positions_phrases =  detect_number_phrases_position(wordlist)
>>> print positions_phrase
>>> print positions_phrases
[(1, 3), (6, 7)]
```

* استخلاص مواضع العبارات العددية باستعمال الوسوم 

 * DO: لاشيء
 * DB: بداية العبارة العددية
 * BI: داخل العبارة العددية

Detect number words in a text and return a taglist as BIO.

```python
>>> wordlist = araby.tokenize(u"وجدت خمسمئة وثلاثة وعشرين دينارا فاشتريت ثلاثة عشر دفترا")
>>> detect_numbers(wordlist)
['DO', 'DB', 'DI', 'DI', 'DO', 'DO', 'DB', 'DI', 'DO']
```

* استخلاص العبارات العددية وإرجاع الجمل

Detect number words in a text, return strings.

```python
>>> detect_number_words(u"وجدت خمسمئة وثلاثة وعشرين دينارا")
خمسمئة وثلاثة وعشرين
```
* تشكيل أولي للعبارات العددية

Vocalized a number clauses in a text.

```python
>>> txt = u"وجدت خمسمئة وثلاثة وعشرين دينارا فاشتريت ثلاثة عشر دفترا"
>>> wordlist = araby.tokenize(txt)
>>> vocalized =  pre_tashkeel_number(wordlist)
>>> print u" ".join(vocalized)
وجدت خَمْسمِئَة وَثَلاثَة وَعِشْرِينَ دينارا فاشتريت ثَلاثَةَ عَشَرَ دفترا
```


#### وظائف قلب النصوص
تستعمل لقلب الحروف، بسبب عدم دعم بعض البرامج للغة العربية، مما يدعونا إلى قلب الحروف.

* قلب النص 

Unshape a text

```python 
>>> TEXTS = u'لو والحيـاة مريرة   وليتك ترضى والانـــام غضاب '
>>> print unshaping_text(TEXTS).encode('utf8')
باضغ ماـــنالاو ىضرت كتيلو   ةريرم ةاـيحلاو ولحت كتيلف

```
* قلب سطر

Unshape a line

```python
>>> line = u'فليتك تحلو والحيـاة مريرة   وليتك ترضى والانـــام غضاب '
>>> print unshaping_line(line).encode('utf8')
باضغ ماـــنالاو ىضرت كتيلو   ةريرم ةاـيحلاو ولحت كتيلف

```
* قلب كلمة

Unshape a word
```python
>>> word = u'العربية'
>>> print unshaping_word(word).encode('utf8')
ةيبرعلا
```

