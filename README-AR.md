# معرض السلام — نسخة موبايل Android

هذا المشروع يحوّل نسخة HTML الحالية إلى تطبيق Android باستخدام Capacitor، مع استخدام اللوجو الجديد كأيقونة للتطبيق.

## الملفات الأساسية

- `www/index.html` — الموقع/التطبيق الحالي.
- `www/app-icon.png` — نسخة اللوجو داخل واجهة الويب.
- `www/manifest.webmanifest` — إعدادات PWA للأجهزة التي تدعم التثبيت من المتصفح.
- `assets/icon.png` — المصدر الذي يستخدمه مولّد أيقونات Capacitor.
- `capacitor.config.ts` — اسم التطبيق وPackage ID ومجلد الويب.
- `package.json` — مكتبات وأوامر Capacitor.
- `.github/workflows/build-android.yml` — يبني APK تلقائيًا على GitHub Actions.

## إنشاء مشروع Android محليًا

يتطلب Capacitor حاليًا Node.js 22+ وAndroid Studio/Android SDK لإنشاء وبناء تطبيق Android.

```bash
npm install
npm run cap:add:android
npm run assets:android
npx cap sync android
npx cap open android
```

بعدها من Android Studio يمكن تشغيل التطبيق على جهاز Android أو Emulator ثم إنشاء APK/Bundle.

## البناء تلقائيًا من GitHub

ارفع محتويات المجلد إلى المستودع، ثم افتح تبويب **Actions** وشغّل workflow باسم **Build Android APK**. بعد انتهاء البناء ستجد ملف APK داخل Artifacts.
