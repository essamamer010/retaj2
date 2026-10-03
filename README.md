# موقع الريتاج — نسخة مستقلة (بدون Base44)

## الخطوات (على جهازك، مرة واحدة)

1. ثبّت Node.js (نسخة LTS) من nodejs.org
2. افتح الـ Terminal داخل فولدر المشروع ونفّذ بالترتيب:

   npm install
   npm run images     # ينزّل كل الصور من Base44 إلى public/images (لازم قبل ما تقفل اشتراك Base44)
   npm run build      # ينتج فولدر dist

3. افتح cPanel ← File Manager ← public_html، وارفع **محتوى** فولدر dist (مش الفولدر نفسه).
   تأكد إن ملف .htaccess اتنقل (فعّل Show Hidden Files).
4. الفورم: ملف send-inquiry.php (موجود جوه dist) بيبعت الطلبات على info@retaj-egy.com.
   لازم يكون في إيميل على نفس الدومين، وجرّب إرسال طلب بعد الرفع.

## تعديل المحتوى
- الماكينات: src/data/machines.json
- الأحبار: src/data/toners.json
- بيانات الشركة (تليفون، واتساب، عنوان): src/lib/site.js
بعد أي تعديل: npm run build ثم ارفع dist من جديد.
