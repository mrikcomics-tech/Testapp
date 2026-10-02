# تطبيق إدارة الزبائن - نسخة Android مستقلة

هذه النسخة تضع ملفات واجهة التطبيق داخل APK نفسه:
- لا تعتمد على GitHub Pages لتشغيل الواجهة.
- ملفات HTML/CSS/JavaScript موجودة داخل `app/src/main/assets`.
- تبقى المزامنة مع Google Apps Script كما هي في `app.js` عند توفر الإنترنت.

## البناء
المشروع Android/Gradle. يمكن فتحه في Android Studio ثم Build > Generate Signed Bundle / APK.

مهم:
- لا تحذف نسخة GitHub الحالية حتى يتم اختبار APK الجديد.
- لا تغيّر `SYNC_URL` و`SYNC_TOKEN` في `app.js` إلا إذا كنت تريد تغيير خادم المزامنة.
- التطبيق يحتاج الإنترنت فقط عندما تستخدم المزامنة مع Google Apps Script؛ الواجهة والبيانات المحلية تعملان داخل الجهاز.
