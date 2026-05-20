<div align="center">
📱 Termux Customizer
</div>
<div align="center">
#📱 أداة تخصيص واجهة Termux
</div>
<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-green?style=for-the-badge&logo=python)
![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20Termux-brightgreen?style=for-the-badge&logo=android)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![Version](https://img.shields.io/badge/Version-1.0-orange?style=for-the-badge)
![Arabic](https://img.shields.io/badge/Arabic-Support-red?style=for-the-badge)

**أداة تفاعلية لتخصيص واجهة Termux بالكامل من القوائم**

*Interactive CLI tool to fully customize your Termux terminal interface*

</div>

---

## ✨ المميزات / Features

| الميزة | التفاصيل |
|--------|----------|
| 🎨 **بانرات ASCII** | أكثر من 45 بانر مختلف |
| 🌈 **ثيمات الألوان** | 10 ثيمات جاهزة (Matrix, Dracula, Nord...) |
| 🖼️ **إطارات الشاشة** | 20 شكل إطار مختلف |
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

## 📱 متطلبات التشغيل / Requirements

```bash
# Termux مطلوب تثبيته على Android
pkg update && pkg upgrade -y
pkg install python -y

# مكتبات العربية (مطلوبة لعرض النص العربي بشكل صحيح)
pkg install rust -y
pip install arabic-reshaper
pip install python-bidi==0.4.2
```

---

## 🚀 طريقة التشغيل / Installation & Run

### الطريقة الأولى — تحميل مباشر:
```bash
# اعطِ Termux صلاحية الوصول للتخزين
termux-setup-storage

# شغّل الأداة من مجلد التنزيلات
cd /sdcard/Download
python mud_tc.py
```

### الطريقة الثانية — اختصار دائم:
```bash
# أضف alias في ~/.bashrc
echo "alias tc='cd /sdcard/Download && python mud_tc.py'" >> ~/.bashrc
source ~/.bashrc

# من الآن فصاعداً شغّلها بـ:
tc
```

---

## 📖 طريقة الاستخدام / Usage

```
╔══════════════════════════════════════════╗
║       Termux Customizer  v1.0            ║
║       أداة تخصيص واجهة Termux           ║
╚══════════════════════════════════════════╝

القائمة الرئيسية:
  [1]  اختيار البانر  (ASCII Art)
  [2]  اختيار ثيم الألوان
  [3]  اختيار شكل البروميت
  [4]  اختيار الخط
  [5]  تخصيص رسالة الترحيب
  [6]  إضافات (تاريخ، وقت، بطارية...)
  [B]  إطارات الشاشة (Borders)
  [C]  ألوان الخلفية والخط
  [7]  معاينة النتيجة
  [8]  تطبيق وحفظ في ~/.bashrc
  [9]  تثبيت الخط المختار
  [R]  إعادة ضبط المصنع
  [0]  خروج
```

### نظام التنقل:
- اكتب رقم الخيار لـ **معاينته**
- `[Y]` للتأكيد و `[N]` للرجوع للقائمة السابقة
- `[N]` في أي قائمة = بدون تخصيص (افتراضي Termux)
- `[0]` = رجوع للقائمة الرئيسية

---

## 🎨 البانرات المتوفرة / Available Banners

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

## 🌈 الثيمات المتوفرة / Available Themes

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
| Solarized | أزرق وبيج |
| Monokai | أخضر وبنفسجي |

---

## ⚙️ كيف يعمل / How It Works

الأداة تولّد كود Bash وتحفظه في `~/.bashrc`:

```bash
# مثال على الكود المولّد
echo -e "\e[1m"
cat << 'TERMUX_BANNER'
██╗  ██╗ █████╗  ██████╗██╗  ██╗
...
TERMUX_BANNER

echo -e "مرحباً بك في Termux!"
echo -e "$(date '+%A %d %B %Y')"

export PS1="\[\e[1;32m\]\u@\h\[\e[0m\]:\[\e[1;34m\]\w\[\e[1;32m\] ▶ \[\e[0m\]"
```

---

## 📂 هيكل الملف / File Structure

```
termux-customizer/
├── mud_tc.py          # الأداة الرئيسية
└── README.md          # هذا الملف
```

---

## 🔧 المشاكل الشائعة / Troubleshooting

| المشكلة | الحل |
|---------|------|
| النص العربي معكوس | `pip install arabic-reshaper python-bidi` |
| خطأ `ModuleNotFoundError` | `pip install arabic-reshaper python-bidi==0.4.2` |
| لا يظهر التغيير بعد التطبيق | `source ~/.bashrc` |
| خطأ في الصلاحيات | `termux-setup-storage` |
| `python: command not found` | `pkg install python` |

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
Free to use with attribution
```

---

<div align="center">

⭐ **إذا أعجبتك الأداة، لا تنسَ النجمة!**
*If you found this useful, please star the repo!* ⭐

</div>
