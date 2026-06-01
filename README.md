<div align="center">
 📱 أداة تخصيص واجهة Termux


*꧁ঔৣ☬ Muhannad Daher ☬ঔৣ꧂*

*أداة تفاعلية لتخصيص واجهة Termux بالكامل من القوائم*

---

![Version](https://img.shields.io/badge/1.0-%EF%BA%8D%EF%BB%B9%EF%BA%BB%EF%BA%AA%EF%BA%8D%EF%BA%AE-blue?style=for-the-badge)<br>
![Platform](https://img.shields.io/badge/%EF%BA%84%EF%BB%A7%EF%BA%AA%EF%BA%AE%EF%BB%AE%EF%BB%B3%EF%BA%AA-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=android)<br>
![Python](https://img.shields.io/badge/3.x-%EF%BA%91%EF%BA%8E%EF%BB%B3%EF%BA%9C%EF%BB%AE%EF%BB%A6-blue?style=for-the-badge&logo=python)<br>
![License](https://img.shields.io/badge/MIT-%EF%BA%8D%EF%BB%9F%EF%BA%98%EF%BA%AE%EF%BA%A7%EF%BB%B4%EF%BA%BA-red?style=for-the-badge)<br>
![Status](https://img.shields.io/badge/%EF%BB%A7%EF%BA%B8%EF%BB%82-%EF%BA%8D%EF%BB%9F%EF%BA%A4%EF%BA%8E%EF%BB%9F%EF%BA%94-blue?style=for-the-badge)

---
***المحتويات***
</div>


- [المميزات](#-المميزات)
- [متطلبات التشغيل](#-متطلبات-التشغيل)
- [التثبيت](#-التثبيت)
- [التثبيت بأمر واحد](https://github.com/mmuhacker/termux-customizer/blob/main/README.md#%D8%A7%D9%84%D8%AA%D8%AB%D8%A8%D9%8A%D8%AA-%D8%A8%D8%A3%D9%85%D8%B1-%D9%88%D8%A7%D8%AD%D8%AF)
- [طريقة الاستخدام](#-طريقة-الاستخدام)
- [نظام التنقل](#-نظام-التنقل)
- [البانرات](#-البانرات-٤٥-بانر)
- [الثيمات](#-الثيمات)
- [المشاكل الشائعة](#-المشاكل-الشائعة)
- [هيكل المستودع](#-هيكل-المستودع)
- [المطوّر](https://github.com/mmuhacker/termux-customizer/blob/main/README.md#%E2%80%8D-%D8%A7%D9%84%D9%85%D8%B7%D9%88%D8%B1)
- [الرخصة](#-الرخصة)

---
<div align="center">
 
## ✨ المميزات



| الميزة | التفاصيل |
|--------|----------|
| 🎨 **بانرات ASCII** | أكثر من 45 بانر مختلف |
| 🌈 **ثيمات الألوان** | 10 ثيمات جاهزة (Matrix, Dracula, Nord...) |
| 🎨 **ألوان الخلفية** | 15 لون للخلفية |
| ✏️ **ألوان الخط** | 20 لون للخط |
| ⌨️ **شكل البروميت** | 7 أشكال (Arrow, Lambda, Git...) |
| 🔤 **الخطوط** | 8 خطوط Nerd Fonts |
| 💬 **رسالة ترحيب** | قابلة للتخصيص بالعربي والإنجليزي |
| 📅 **إضافات** | تاريخ، وقت، بطارية، تخزين، uptime |
| 💾 **حفظ تلقائي** | تطبيق مباشر على `~/.bashrc` مع نسخة احتياطية |
| 🔄 **إعادة ضبط** | إرجاع كل شيء لافتراضي Termux |
| 🌐 **دعم العربية** | واجهة عربية كاملة مع RTL صحيح |

---

## 📱 متطلبات التشغيل
</div>


**1. تحديث الحزم:**
```bash
pkg update && pkg upgrade -y
```

**2. تثبيت Python:**
```bash
pkg install python -y
```

**3. تثبيت Rust (مطلوب للمكتبات):**
```bash
pkg install rust -y
```

**4. تثبيت مكتبة arabic-reshaper:**
```bash
pip install arabic-reshaper
```

**5. تثبيت مكتبة python-bidi:**
```bash
pip install python-bidi==0.4.2
```

**تثبيت الخط العربي (مرة واحدة إذا لم يكن مثبتاً)**
```bash
curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf
termux-reload-settings
```
---

<div align="center">

## 🚀 التثبيت

</div>

**1. تحميل الأداة وتثبيتها في المجلد الأساسي:**
```bash
curl -o $PREFIX/bin/mud_tc.py https://raw.githubusercontent.com/mmuhacker/termux-customizer/main/mud_tc.py
```

**2. إعطاء الأداة صلاحيات التنفيذ:**
```bash
chmod +x $PREFIX/bin/mud_tc.py
```

**3. إنشاء الإختصار tc ليتم تشغيل الأداة عند كتابته:**

**نفذ هذا الأمر:**
```bash
ln -sf $PREFIX/bin/mud_tc.py $PREFIX/bin/tc
```
*قم بتشغيل الأداة بكتابة الإختصار*

**4. تشغيل الأداة:**
```bash
tc
```
---
<div align="center">
 
## التثبيت بأمر واحد
</div>

```bash
pkg update && pkg install python curl -y && pip install arabic-reshaper python-bidi --break-system-packages && curl -o $PREFIX/bin/mud_tc.py https://raw.githubusercontent.com/mmuhacker/termux-customizer/main/mud_tc.py && chmod +x $PREFIX/bin/mud_tc.py && ln -sf $PREFIX/bin/mud_tc.py $PREFIX/bin/tc && mkdir -p ~/.termux && curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf && termux-reload-settings && echo "تم التثبيت بنجاح! الأداة جاهزة (tc) والخط العربي تم تفعيله."

```
**بهذا يكون تم تثبيت كل ما تحتاجه الأداة لتشغيلها**

---

<div align="center">

## 📖 طريقة الاستخدام

```

╔════════════════════════╗
║                            ║
║   Termux Customizer  v1.0  ║
║                            ║
╚════════════════════════╝

```
</div>



- [1]  اختيار البانر  (ASCII Art)
- [2]  اختيار ثيم الألوان
- [3]  اختيار شكل البروميت
- [4]  اختيار الخط
- [5]  تخصيص رسالة الترحيب
- [6]  إضافات (تاريخ، وقت، بطارية...)
- [C]  ألوان الخلفية والخط
- [7]  معاينة النتيجة
- [8]  تطبيق وحفظ في ~/.bashrc
- [9]  تثبيت الخط المختار
- [R]  إعادة ضبط المصنع
- [0]  خروج


---

<div align="center">
 
### نظام التنقل:

</div>

- اكتب رقم الخيار لـ **معاينته أولاً**
- `[Y]` للتأكيد — `[N]` للرجوع للقائمة السابقة
- `[N]` في أي قائمة = بدون تخصيص (افتراضي Termux)
- `[0]` = رجوع للقائمة الرئيسية

---
<div align="center">
## 🎨 البانرات ٤٥ بانر
</div>

```
HACK • TERMUX • MATRIX • Dragon • Cat • Robot
مرحباً (عربي) • Box Style • Stars • Skull • Minimal
Fire • Cyberpunk • Glitch • Android • Sword • UFO
Pyramid • Diamond • Lock • Planet • Crown • Terminal
Worm • Ninja • Ghost • Eagle • Snake • Wolf • Binary
Compass • Rocket • Wave • Double Box • Dots Art
Flame • Samurai • Shield • Anarchy • Eye • Mushroom
Pixel Heart • ... والمزيد
```

---

<div align="center">

## 🌈 الثيمات

| الثيم | الألوان |
|-------|---------|
| Matrix 🟢 | أخضر على أسود |
| Synthwave 💜 | بنفسجي ووردي |
| Ocean 🔵 | أزرق وسماوي |
| Gold 👑 | ذهبي على أسود |
| Dracula 🧛 | بنفسجي وأزرق |
| Nord ❄ | أبيض وسماوي |
| Fire 🔥 | أحمر وبرتقالي |
| Gruvbox 🟤 | بيج وذهبي |
| Red 🔴 | أحمر |
| White ⚪ | أبيض |

---

## 🔧 المشاكل الشائعة

| المشكلة | الحل |
|---------|------|
| النص العربي معكوس | `pip install arabic-reshaper python-bidi` |
| خطأ `ModuleNotFoundError` | `pip install python-bidi==0.4.2` |
| لا يظهر التغيير | `source ~/.bashrc` |
| خطأ في الصلاحيات | `termux-setup-storage` |
| `python: not found` | `pkg install python` |

---

## 📂 هيكل المستودع

```
termux-customizer/
├── mud_tc.py     # الأداة الرئيسية
└── README.md     # هذا الملف
```
---


## 👨‍💻 المطور



**Muhannad Daher**
[![GitHub](https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github)](https://github.com/mmuhacker)

---

## 📄 الرخصة
MIT License — حر الاستخدام مع ذكر المصدر

---
</div>

- أداة تخصيص واجهة تيرموكس Termux
- البيئة: Termux (Android)
- الإصدار: v1.0



---
<div align="center">

⭐ **إذا أعجبتك الأداة، لا تنسَ النجمة!** ⭐
</div>
