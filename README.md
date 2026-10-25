# 🚌 HIAST.Transportation

> نظام إدارة النقل، ويتكوّن من واجهة ويب إدارية (Frontend) وخدمات خلفية (Backend) مستقلّة.

هذا المستودع هو **المستودع الرئيسي (Superproject)** الذي يجمع المستودعين البرمجيين كـ **Git Submodules**. تبقى شيفرة كل مشروع وسجل Git الخاص به في مستودعه الأصلي، ويمكن فتحه مباشرةً بالنقر على اسمه في قائمة الملفات في GitHub.

## 📁 هيكلية المستودع

- [📁 HIAST.Transportation.UI](https://github.com/ahmadabdelbary2001/HIAST.Transportation.UI) — واجهة المستخدم المبنية باستخدام React وTypeScript وVite.
- [📁 HIAST.Transportation.Clean](https://github.com/ahmadabdelbary2001/HIAST.Transportation.Clean) — الواجهة الخلفية المبنية باستخدام ASP.NET Core و.NET 9.
- `README.md` — الصفحة الرئيسية التي تعرّف بالنظام وتربط مكوّناته.

> ملاحظة: المجلدان أعلاه هما Git Submodules وليسا نسختين من ملفات المشروع داخل المستودع الرئيسي. كل واحد يشير إلى commit محدد من المستودع الأصلي، ويمكن تحديث مرجعه عند الحاجة.

## 🧩 نظرة عامة على المعمارية

```text
HIAST.Transportation
├── HIAST.Transportation.UI       → React / TypeScript frontend repository
├── HIAST.Transportation.Clean    → ASP.NET Core backend repository
└── README.md                     → Main project overview
```

تتواصل الواجهة الأمامية مع الباك إند عبر HTTP API، وتستخدم SignalR للإشعارات الفورية. راجع إعدادات Vite وتهيئة API في المستودعين لمعرفة إعدادات التطوير الحالية.

## 🚀 استنساخ المستودع كاملًا

لتحميل المستودع الرئيسي والمشروعين المرتبطين به، استخدم:

```bash
git clone --recurse-submodules https://github.com/ahmadabdelbary2001/HIAST.Transportation.git
cd HIAST.Transportation
```

إذا استنسخت المستودع دون `--recurse-submodules`، فيمكن تحميل مكوّناته لاحقًا باستخدام:

```bash
git submodule update --init --recursive
```

## 🔄 تحديث مراجع المشاريع

المستودع الرئيسي يثبّت كل Submodule على commit محدد؛ لذا لا يتغيّر مرجعه تلقائيًا بمجرد تحديث المستودع الأصلي. لتحديث المرجعين إلى آخر commit في فرع `main`:

```bash
git submodule update --remote --merge
git status
git add HIAST.Transportation.UI HIAST.Transportation.Clean
git commit -m "chore: update project submodules"
git push
```

## 🔗 المستودعات الأصلية

- **Frontend:** [HIAST.Transportation.UI](https://github.com/ahmadabdelbary2001/HIAST.Transportation.UI)
- **Backend:** [HIAST.Transportation.Clean](https://github.com/ahmadabdelbary2001/HIAST.Transportation.Clean)

---

<p align="center">Made with ❤️ by <a href="https://github.com/ahmadabdelbary2001">Ahmad Abdelbary</a></p>
