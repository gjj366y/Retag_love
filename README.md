
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ريتاج - حب أبدي</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(45deg, #ff7eb9, #feb47b);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      color: #fff;
      overflow: hidden;
      width: 100%;
    }

    .container {
      text-align: center;
      animation: fadeInUp 1s ease-out forwards;
      opacity: 0;
      text-shadow: 0 0 15px rgba(255, 255, 255, 0.8);
      width: 100%;
      padding: 20px;
      box-sizing: border-box;
      max-width: 100%;
      margin: 0 auto;
    }

    h1 {
      font-size: 28px;
      margin-bottom: 20px;
      animation-delay: 0.5s;
      color: #ffccff;
    }

    p {
      font-size: 18px;
      animation-delay: 1s;
      line-height: 1.5;
      color: #ffebcd;
      margin-bottom: 20px;
    }

    .button {
      background-color: #ff0066;
      color: white;
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin: 10px 0;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s ease;
      width: 100%;
      max-width: 300px;
    }

    .button:hover {
      transform: scale(1.1);
    }

    .hidden {
      display: none;
    }

    .question {
      font-size: 20px;
      margin-top: 20px;
    }

    @keyframes fadeInUp {
      0% {
        opacity: 0;
        transform: translateY(30px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 480px) {
      h1 {
        font-size: 24px;
      }

      p {
        font-size: 16px;
      }

      .button {
        font-size: 16px;
        padding: 12px 25px;
        max-width: 90%;
      }

      .question {
        font-size: 18px;
      }
    }

    @media (max-width: 320px) {
      .button {
        font-size: 14px;
        padding: 10px 20px;
      }

      h1 {
        font-size: 20px;
      }

      p {
        font-size: 14px;
      }

      .question {
        font-size: 16px;
      }
    }
  </style>
</head>
<body>

  <div class="container" id="page1">
    <h1>أهلاً ياعمري يا ريتاج</h1>
    <p>أنتِ نبضي، وهدوء روحي، وكل لحظة حلوة في حياتي.</p>
    <p>يا من زينتِ عالمي بوجودك، وكل لحظة معك هي أجمل من الأخرى.</p>
    <p>أنتِ الحلم الجميل الذي تحقق في حياتي.</p>
    <p>أنتِ الأمل الذي أعيش من أجله، أحبك بكل تفاصيلك يا ريتاج.</p>
    <button class="button" onclick="goToPage2()">اضغطي هنا يا روحي</button>
  </div>

  <div class="container hidden" id="page2">
    <h1>أسئلة صبحي</h1>
    <p class="question">كم عمر صبحي؟</p>
    <button class="button" onclick="showQuestion2()">١٦</button>
    <button class="button" onclick="showQuestion2()">١٧</button>
    <button class="button" onclick="showQuestion2()">١٨</button>
  </div>

  <div class="container hidden" id="question2">
    <p class="question">أفضل أكلة لدى صبحي؟</p>
    <button class="button" onclick="showQuestion3()">ملوخية</button>
    <button class="button" onclick="showQuestion3()">كبسة دجاج</button>
    <button class="button" onclick="showQuestion3()">جميع ما سبق</button>
  </div>

  <div class="container hidden" id="question3">
    <p class="question">هل صبحي يفضل السكر على ريتاج؟</p>
    <button class="button" onclick="showQuestion4()">نعم</button>
    <button class="button" onclick="showQuestion4()">لا</button>
  </div>

  <div class="container hidden" id="question4">
    <p class="question">هل صبحي يعشق ريتاج؟</p>
    <button class="button" onclick="showQuestion5()">نعم</button>
    <button class="button" onclick="showQuestion5()">لا</button>
  </div>

  <div class="container hidden" id="question5">
    <p class="question">أين يكون صبحي الساعة ١٢:٠٠؟</p>
    <button class="button" onclick="finish()">بالبيت نايم</button>
    <button class="button" onclick="finish()">طالع مع أصدقائه</button>
  </div>

  <!-- صفحة ارسال الإجابات -->
  <div class="container hidden" id="finishPage">
    <h1>تم الإجابة على الأسئلة!</h1>
    <p>إرسال الإجابات إلى صبحي:</p>
    <button class="button" onclick="sendToWhatsApp()">إرسال إلى صبحي عبر واتساب</button>
    <button class="button" onclick="sendToInstagram()">إرسال إلى صبحي عبر إنستغرام</button>
    <button class="button" onclick="shareResults()">مشاركة النتائج عبر التطبيقات</button>
    <button class="button" onclick="copyResults()">نسخ النتائج</button>
  </div>

  <script>
    // الانتقال بين الصفحات
    function goToPage2() {
      document.getElementById('page1').classList.add('hidden');
      document.getElementById('page2').classList.remove('hidden');
    }

    function showQuestion2() {
      document.getElementById('page2').classList.add('hidden');
      document.getElementById('question2').classList.remove('hidden');
    }

    function showQuestion3() {
      document.getElementById('question2').classList.add('hidden');
      document.getElementById('question3').classList.remove('hidden');
    }

    function showQuestion4() {
      document.getElementById('question3').classList.add('hidden');
      document.getElementById('question4').classList.remove('hidden');
    }

    function showQuestion5() {
      document.getElementById('question4').classList.add('hidden');
      document.getElementById('question5').classList.remove('hidden');
    }

    function finish() {
      document.getElementById('question5').classList.add('hidden');
      document.getElementById('finishPage').classList.remove('hidden');
    }

    // إرسال الإجابات إلى صبحي عبر واتساب
    function sendToWhatsApp() {
      const answers = {
        age: "١٦",  // على سبيل المثال
        favoriteDish: "جميع ما سبق",  // على سبيل المثال
        prefersSugar: "لا يفضل ريتاج عن السكر",
        lovesRetaj: "نعم",
        location: "بالبيت نايم"
      };

      const message = `إجابات الأسئلة:\n
        ١. كم عمر صبحي؟: ${answers.age}\n
        ٢. أفضل أكلة لدى صبحي؟: ${answers.favoriteDish}\n
        ٣. هل صبحي يفضل السكر على ريتاج؟: ${answers.prefersSugar}\n
        ٤. هل صبحي يعشق ريتاج؟: ${answers.lovesRetaj}\n
        ٥. أين يكون صبحي الساعة ١٢:٠٠؟: ${answers.location}`;

      const whatsappUrl = `https://wa.me/966557073705?text=${encodeURIComponent(message)}`;
      window.open(whatsappUrl, "_blank");
    }

    // إرسال الإجابات إلى صبحي عبر إنستغرام
    function sendToInstagram() {
      const message = `إجابات الأسئلة:  
        ١. كم عمر صبحي؟: ١٦  
        ٢. أفضل أكلة لدى صبحي؟: جميع ما سبق  
        ٣. هل صبحي يفضل السكر على ريتاج؟: لا يفضل ريتاج عن السكر  
        ٤. هل صبحي يعشق ريتاج؟: نعم  
        ٥. أين يكون صبحي الساعة ١٢:٠٠؟: بالبيت نايم`;

      const instagramUrl = `https://www.instagram.com/messages/compose/?text=${encodeURIComponent(message)}`;
      window.open(instagramUrl, "_blank");
    }

    // مشاركة النتائج عبر التطبيقات
    function shareResults() {
      const message = `إجابات الأسئلة:\n
        ١. كم عمر صبحي؟: ١٦\n
        ٢. أفضل أكلة لدى صبحي؟: جميع ما سبق\n
        ٣. هل صبحي يفضل السكر على ريتاج؟: لا يفضل ريتاج عن السكر\n
        ٤. هل صبحي يعشق ريتاج؟: نعم\n
        ٥. أين يكون صبحي الساعة ١٢:٠٠؟: بالبيت نايم`;

      if (navigator.share) {
        navigator.share({
          title: 'إجابات الأسئلة',
          text: message,
          url: window.location.href
        }).catch((error) => console.log