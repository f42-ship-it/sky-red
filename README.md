# Sky Red – iOS App

متجر تطبيقات بريميوم مبني بـ Capacitor

---

## المتطلبات
- Mac مع macOS 12+
- Xcode 14+
- Node.js 16+
- CocoaPods

---

## خطوات التثبيت

### 1. تثبيت المكتبات
```bash
cd skyred_app
npm install
```

### 2. مزامنة مع iOS
```bash
npx cap sync ios
```

### 3. تثبيت CocoaPods
```bash
cd ios/App
pod install
cd ../..
```

### 4. فتح في Xcode
```bash
npx cap open ios
```

---

## في Xcode

1. اختر Team من **Signing & Capabilities** (Apple ID مجاني يكفي للتجربة)
2. اختر جهازك أو Simulator
3. اضغط ▶️ Run

---

## هيكل المشروع

```
skyred_app/
├── www/                    ← الشاشات
│   ├── index.html          ← نقطة البداية
│   ├── splash.html         ← شاشة البداية (3 ثوانٍ ثم home)
│   ├── home.html           ← الرئيسية
│   ├── categories.html     ← الفئات
│   ├── downloads.html      ← التنزيلات
│   └── app-details.html    ← تفاصيل التطبيق
├── ios/                    ← مشروع Xcode
├── capacitor.config.json   ← إعدادات Capacitor
└── package.json
```

---

## الشاشات والتنقل

```
Splash (3s) → Home ↔ Categories ↔ Downloads
                          ↓
                     App Details
```

---

## ملاحظات
- التطبيق يدعم iPhone notch و Dynamic Island تلقائياً
- الـ Status Bar داكنة تناسب الثيم
- Portrait فقط (مناسب لمتجر التطبيقات)
