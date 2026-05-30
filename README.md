<div align="center">

# 🌍 IP Info Lookup — أداة معلومات عنوان IP

**تعمل على نظام Kali Linux و تطبيق Termux**

꧁ঔৣ☬ Muhannad Daher ☬ঔৣ꧂

---

![Version](https://img.shields.io/badge/Version-1.0-blue?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Kali_Linux-green?style=for-the-badge&logo=kalilinux)
![Platform](https://img.shields.io/badge/Platform-Android-green?style=for-the-badge&logo=android)
![Python](https://img.shields.io/badge/Python-3.x-yellow?style=for-the-badge&logo=python)
![License](https://img.shields.io/badge/License-MIT_License-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

---

**المحتويات:**

</div>

- [الوصف](#الوصف)
- [المميزات](#المميزات)
- [التثبيت على Termux](#التثبيت-على-termux)
- [التثبيت على Kali Linux](#التثبيت-على-kali-linux)
- [التشغيل](#التشغيل)
- [طريقة الاستخدام](#طريقة-الاستخدام)
- [مثال](#مثال)
- [المتطلبات](#المتطلبات)
- [إخلاء المسؤولية](#إخلاء-المسؤولية)
- [المطوّر](#المطوّر)

---

<div align="center" id="الوصف">

## 📌 الوصف

</div>

أداة للحصول على معلومات تفصيلية عن أي عنوان IP أو نطاق، مكتوبة بلغة Python وتعمل على Termux و Kali Linux. تعرض الدولة والمدينة ومزود الخدمة والإحداثيات الجغرافية مع رابط مباشر لخرائط Google.

---

<div align="center" id="المميزات">

## ✨ المميزات

</div>

- 🌍 عرض الدولة والمنطقة والمدينة والرمز البريدي
- 📡 عرض مزود الخدمة ISP والمنظمة
- 📍 الإحداثيات الجغرافية مع رابط خرائط Google
- 🕐 المنطقة الزمنية ورقم AS
- 💻 معلومات عن IP جهازك الحالي
- 🔄 تحويل النطاق إلى IP تلقائياً
- 🌍 واجهة عربية بالكامل

---

<div align="center" id="التثبيت-على-termux">

## ⚙️ التثبيت

### Termux

</div>

**الخطوة 1 — تحديث النظام**
```bash
pkg update && pkg upgrade -y
```

**الخطوة 2 — تثبيت المتطلبات** *(لمرة واحدة فقط)*
```bash
pkg install python tor curl fontconfig rust -y
```
```bash
pip install requests pysocks arabic-reshaper
pip install python-bidi==0.4.2
```

**الخطوة 3 — تثبيت الخط العربي** *(لمرة واحدة فقط)*
```bash
curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf
termux-reload-settings
```

**الخطوة 4 — تنزيل الأداة**
```bash
curl -o $PREFIX/bin/mud_ii.py https://raw.githubusercontent.com/mmuhacker/mud-ii/main/mud_ii.py
```

**الخطوة 5 — إعطاء صلاحية التشغيل**
```bash
chmod +x $PREFIX/bin/mud_ii.py
```

**الخطوة 6 — إنشاء رابط الاختصار**
```bash
ln -sf $PREFIX/bin/mud_ii.py $PREFIX/bin/ii
```

**⚡ أو قم بكل شيء بأمر واحد مجمّع**
```bash
pkg update && pkg upgrade -y && pkg install python tor curl fontconfig rust -y && pip install requests pysocks arabic-reshaper && pip install python-bidi==0.4.2 && curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf && termux-reload-settings && curl -o $PREFIX/bin/mud_ii.py https://raw.githubusercontent.com/mmuhacker/mud-ii/main/mud_ii.py && chmod +x $PREFIX/bin/mud_ii.py && ln -sf $PREFIX/bin/mud_ii.py $PREFIX/bin/ii && ii
```

---

<div align="center" id="التثبيت-على-kali-linux">

### Kali Linux

</div>

**الخطوة 1 — تحديث النظام**
```bash
sudo apt update && sudo apt upgrade -y
```

**الخطوة 2 — تثبيت المتطلبات** *(لمرة واحدة فقط)*
```bash
pip install requests arabic-reshaper python-bidi==0.4.2 --break-system-packages
```

**الخطوة 3 — تنزيل الأداة**
```bash
sudo curl -o /usr/local/bin/mud_ii.py https://raw.githubusercontent.com/mmuhacker/mud-ii/main/mud_ii.py
```

**الخطوة 4 — إعطاء صلاحية التشغيل**
```bash
sudo chmod +x /usr/local/bin/mud_ii.py
```

**الخطوة 5 — إنشاء رابط الاختصار**
```bash
sudo ln -sf /usr/local/bin/mud_ii.py /usr/local/bin/ii
```

**⚡ أو قم بكل شيء بأمر واحد مجمّع**
```bash
sudo apt update && sudo apt upgrade -y && pip install requests arabic-reshaper python-bidi==0.4.2 --break-system-packages && sudo curl -o /usr/local/bin/mud_ii.py https://raw.githubusercontent.com/mmuhacker/mud-ii/main/mud_ii.py && sudo chmod +x /usr/local/bin/mud_ii.py && sudo ln -sf /usr/local/bin/mud_ii.py /usr/local/bin/ii && ii
```

---

<div align="center" id="التشغيل">

## 🚀 التشغيل

</div>

```bash
ii
```

**أو بالأمر الكامل**

```bash
mud_ii.py
```

---

<div align="center" id="طريقة-الاستخدام">

## 📖 طريقة الاستخدام


| الوضع | الوصف |
|-------|-------|
| `1` IP أو نطاق | أدخل أي IP مثل `8.8.8.8` أو نطاق مثل `google.com` |
| `2` IP جهازك | عرض معلومات عنوان IP الخاص بجهازك |
| `3` تحويل نطاق | تحويل اسم النطاق إلى عنوان IP |

</div>

---

<div align="center" id="مثال">

## 💡 مثال

</div>


اختيارك: 1
أدخل IP أو نطاق: 8.8.8.8

  🌐  عنوان IP          8.8.8.8
  🏳️  الدولة            United States (US)
  🏙️  المنطقة           California
  🏘️  المدينة           Mountain View
  📮  الرمز البريدي     94043
  📍  الإحداثيات        37.4056, -122.0775
  🕐  المنطقة الزمنية   America/Los_Angeles
  📡  مزود الخدمة       Google LLC
  🏢  المنظمة           Google LLC
  🔢  رقم AS            AS15169 Google LLC

  🗺️  خرائط Google:
  https://maps.google.com/?q=37.4056,-122.0775

---

<div align="center" id="المتطلبات">

## 🔧 المتطلبات



| المتطلب | الوصف |
|---------|-------|
| Python 3.6+ | لغة البرمجة |
| arabic-reshaper | دعم النص العربي |
| python-bidi | اتجاه النص العربي |
| curl | تنزيل الأداة |
| اتصال بالإنترنت | للاستعلام عن معلومات IP |

</div>

> ⚠️ **ملاحظة:** بدون تثبيت `arabic-reshaper` و `python-bidi` سيظهر النص العربي معكوساً ومتقطعاً.

---

<div align="center" id="إخلاء-المسؤولية">

## ⚖️ إخلاء المسؤولية

</div>

هذه الأداة مخصصة **لأغراض تعليمية فقط**.
لا تستخدمها لأغراض غير مشروعة.

---

<div align="center" id="المطوّر">

## 👨‍💻 المطوّر

**Muhannad Daher**

[![GitHub](https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github)](https://github.com/mmuhacker)

---

***Madarik Tools — صُنع بالعربية***

⭐ **إذا أعجبتك الأداة، لا تنسَ النجمة!** ⭐

</div>
