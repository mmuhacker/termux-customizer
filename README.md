<div align="center">
 📱 أداة تخصيص واجهة Termux


*꧁ঔৣ☬ Muhannad Daher ☬ঔৣ꧂*

*أداة تفاعلية لتخصيص واجهة Termux بالكامل من القوائم*

---

![Version](https://img.shields.io/badge/Version-1.0-blue?style=for-the-badge)




![Platform](https://img.shields.io/badge/Platform-Android-green?style=for-the-badge&logo=android)




![Python](https://img.shields.io/badge/Python-3.x-yellow?style=for-the-badge&logo=python)




![License](https://img.shields.io/badge/License-MIT_License-red?style=for-the-badge)




![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)



---
***المحتويات***

- [المميزات](#-المميزات)
- [متطلبات التشغيل](#-متطلبات-التشغيل)
- [التثبيت](#-التثبيت)
- [طريقة الاستخدام](#-طريقة-الاستخدام)
- [نظام التنقل](#-نظام-التنقل)
- [البانرات](#-البانرات-٤٥-بانر)
- [الثيمات](#-الثيمات)
- [المشاكل الشائعة](#-المشاكل-الشائعة)
- [هيكل المستودع](#-هيكل-المستودع)
- [المطوّر](https://github.com/mmuhacker/termux-customizer/blob/main/README.md#%E2%80%8D-%D8%A7%D9%84%D9%85%D8%B7%D9%88%D8%B1)
- [الرخصة](#-الرخصة)

---

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

---

<div align="center">

## 🚀 التثبيت

</div>

**1. تحميل الأداة وإنشاء المجلد:**
```bash
mkdir -p ~/bin && curl -o ~/bin/termux-customizer https://raw.githubusercontent.com/mmuhacker/termux-customizer/main/mud_tc.py
```

**2. إضافة الاختصار:**
```bash
echo "alias tc='python ~/bin/termux-customizer'" >> ~/.bashrc
```

**3. لتطبيق التغييرات فوراً:**

نفذ هذا الأمر:
```bash
source ~/.bashrc
```
**أو أغلق Termux وأعد فتحه.**

**4. تشغيل الأداة:**
```bash
tc
```

---

<div align="center">

## 📖 طريقة الاستخدام

```
╔═══════════════════════════╗
║       Termux Customizer  v1.0  ║
║       by Muhannad Daher        ║
╚═══════════════════════════╝

</div>
  [1]  اختيار البانر  (ASCII Art)
  [2]  اختيار ثيم الألوان
  [3]  اختيار شكل البروميت
  [4]  اختيار الخط
  [5]  تخصيص رسالة الترحيب
  [6]  إضافات (تاريخ، وقت، بطارية...)
  [C]  ألوان الخلفية والخط
  [7]  معاينة النتيجة
  [8]  تطبيق وحفظ في ~/.bashrc
  [9]  تثبيت الخط المختار
  [R]  إعادة ضبط المصنع
  [0]  خروج
```

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
| `tc: not found` | `source ~/.bashrc` ثم أعد المحاولة |

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
[![Contact Us](https://img.shields.io/badge/Contact_Us-black?style=for-the-badge&logo=gmail&logoColor=white)](mailto:madarik.ai.info@gmail.com)

---

## 📄 الرخصة

```
MIT License — حر الاستخدام مع ذكر المصدر
```

---

⭐ **إذا أعجبتك الأداة، لا تنسَ النجمة!** ⭐
</div>
