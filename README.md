<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>قائمتي | My Menu</title>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Cairo', sans-serif;
      background-image: url('your-purple-background.jpg'); /* استبدل هذا لاحقًا بمسار الخلفية */
      background-size: cover;
      background-attachment: fixed;
      background-position: center;
      color: #fff;
    }

    header {
      text-align: center;
      padding: 30px 10px 10px;
    }

    header img {
      max-width: 200px;
    }

    h2 {
      text-align: center;
      margin-top: 40px;
      font-size: 28px;
      color: #fff;
    }

    .pricing {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 40px 20px;
    }

    .card {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(8px);
      border-radius: 15px;
      padding: 25px;
      width: 300px;
      text-align: center;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
    }

    .card h3 {
      font-size: 22px;
      margin-bottom: 10px;
      color: #fff;
    }

    .card p {
      font-size: 20px;
      margin: 10px 0;
      color: #ffd700;
    }

    .card ul {
      text-align: right;
      padding: 0;
      list-style: none;
      margin: 15px 0;
    }

    .card ul li {
      margin: 10px 0;
      border-bottom: 1px solid rgba(255,255,255,0.2);
      padding-bottom: 8px;
    }

    .whatsapp-btn {
      background: #25D366;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      text-decoration: none;
      font-weight: bold;
      display: inline-block;
      margin-top: 15px;
    }

    footer {
      text-align: center;
      padding: 30px 20px;
      font-size: 14px;
      color: rgba(255,255,255,0.7);
    }
  </style>
</head>
<body>

  <header>
    <img src="cleaned_logo.png" alt="شعار قائمتي">
  </header>

  <h2>اختر الباقة المناسبة لمطعمك</h2>

  <section class="pricing">
    <!-- الباقة التجريبية -->
    <div class="card">
      <h3>الباقة التجريبية</h3>
      <p>مجانية</p>
      <ul>
        <li>قائمة إلكترونية بسيطة</li>
        <li>باركود ثابت</li>
        <li>تجربة لمدة 7 أيام</li>
      </ul>
      <a href="https://wa.me/966557073705" target="_blank" class="whatsapp-btn">تواصل عبر واتساب</a>
    </div>

    <!-- الباقة الأساسية -->
    <div class="card">
      <h3>الباقة الأساسية</h3>
      <p>49 ريال / شهريًا</p>
      <ul>
        <li>تصميم خاص للقائمة</li>
        <li>صور وأسعار</li>
        <li>باركود مخصص</li>
        <li>دعم فني</li>
      </ul>
      <a href="https://wa.me/966557073705" target="_blank" class="whatsapp-btn">تواصل عبر واتساب</a>
    </div>

    <!-- الباقة المميزة -->
    <div class="card">
      <h3>الباقة المميزة</h3>
      <p>99 ريال / شهريًا</p>
      <ul>
        <li>جميع ميزات الأساسية</li>
        <li>إحصائيات عدد الزوار</li>
        <li>إدارة عدة فروع</li>
        <li>دعم أولوية</li>
      </ul>
      <a href="https://wa.me/966557073705" target="_blank" class="whatsapp-btn">تواصل عبر واتساب</a>
    </div>
  </section>

  <footer>
    جميع الحقوق محفوظة © 2025 لموقع قائمتي | تصميم صبحي
  </footer>

</body>
</html>