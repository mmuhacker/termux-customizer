<div align="center">
 📱 أداة تخصيص واجهة Termux

꧁ঔৣ☬ Muhannad Daher ☬ঔৣ꧂

*أداة تفاعلية لتخصيص واجهة Termux بالكامل من القوائم*

</div>

---
***المحتويات***
- [المميزات](#-المميزات)
- [متطلبات التشغيل](#-متطلبات-التشغيل)
- [التثبيت](التثبيت)
- [طريقة الاستخدام](طريقة-الاستخدام)
- [نظام التنقل](نظام-التنقل)
- [البانرات](البانرات-٤٥-بانر)

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

## 🚀 التثبيت

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

## 📖 طريقة الاستخدام

```
╔══════════════════════════════════════════╗
║       Termux Customizer  v1.0            ║
║       by Muhannad Daher                  ║
╚══════════════════════════════════════════╝

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

### نظام التنقل:
- اكتب رقم الخيار لـ **معاينته أولاً**
- `[Y]` للتأكيد — `[N]` للرجوع للقائمة السابقة
- `[N]` في أي قائمة = بدون تخصيص (افتراضي Termux)
- `[0]` = رجوع للقائمة الرئيسية

---

## 🎨 البانرات ٤٥ بانر

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

## 🌈 الثيمات / Themes

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

## 🔧 المشاكل الشائعة / Troubleshooting

| المشكلة | الحل |
|---------|------|
| النص العربي معكوس | `pip install arabic-reshaper python-bidi` |
| خطأ `ModuleNotFoundError` | `pip install python-bidi==0.4.2` |
| لا يظهر التغيير | `source ~/.bashrc` |
| خطأ في الصلاحيات | `termux-setup-storage` |
| `python: not found` | `pkg install python` |
| `tc: not found` | `source ~/.bashrc` ثم أعد المحاولة |

---

## 📂 هيكل المستودع / Structure

```
termux-customizer/
├── mud_tc.py     # الأداة الرئيسية
└── README.md     # هذا الملف
```

---

## 👨‍💻 المطوّر / Developer

<div align="center">

**Muhannad Daher**

[![GitHub](https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github)](https://github.com/mmuhacker)

</div>

---

## 📄 الرخصة / License

```
MIT License — حر الاستخدام مع ذكر المصدر
```

---

<div align="center">

⭐ **إذا أعجبتك الأداة، لا تنسَ النجمة!** ⭐

*If you found this useful, please star the repo!*

</div>
