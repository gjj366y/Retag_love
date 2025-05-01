
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
    }

    .container {
      text-align: center;
      animation: fadeInUp 1s ease-out forwards;
      opacity: 0;
      text-shadow: 0 0 15px rgba(255, 255, 255, 0.8);
      padding: 20px;
      box-sizing: border-box;
      max-width: 400px;
      width: 100%;
    }

    h1 {
      font-size: 28px;
      margin-bottom: 20px;
      color: #ffccff;
    }

    p {
      font-size: 18px;
      margin-bottom: 20px;
      color: #ffebcd;
      line-height: 1.5;
    }

    .button {
      background-color: #ff0066;
      color: white;
      padding: 15px;
      margin: 10px 0;
      width: 100%;
      max-width: 300px;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s ease;
    }

    .button:hover {
      transform: scale(1.05);
    }

    .hidden {
      display: none;
    }

    audio {
      display: none;
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>

<body>

  <!-- موسيقى هادئة -->
  <audio autoplay loop>
    <source src="https://dl.sndup.net/ktqr/romantic.mp3" type="audio/mpeg">
    متصفحك لا يدعم تشغيل الصوت.
  </audio>

  <!-- الصفحة الأولى -->
  <div class="container" id="page1">
    <h1>أهلاً يا عمري ريتاج</h1>
    <p>أنتِ نبضي، وهدوء روحي، وكل لحظة حلوة في حياتي.</p>
    <button class="button" onclick="goToPage2()">اضغطي هنا يا روحي</button>
  </div>

  <!-- الأسئلة -->
  <div class="container hidden" id="page2">
    <h1>أسئلة ريتاج</h1>
    <p>كم عمر صبحي؟</p>
    <button class="button" onclick="showQuestion('question2')">١٦</button>
    <button class="button" onclick="showQuestion('question2')">١٧</button>
    <button class="button" onclick="showQuestion('question2')">١٨</button>
  </div>

  <div class="container hidden" id="question2">
    <p>أفضل أكلة لدى صبحي؟</p>
    <button class="button" onclick="showQuestion('question3')">ملوخية</button>
    <button class="button" onclick="showQuestion('question3')">كبسة</button>
    <button class="button" onclick="showQuestion('question3')">جميع ما سبق</button>
  </div>

  <div class="container hidden" id="question3">
    <p>هل صبحي يفضل السكر على ريتاج؟</p>
    <button class="button" onclick="showQuestion('question4')">نعم</button>
    <button class="button" onclick="showQuestion('question4')">لا</button>
  </div>

  <div class="container hidden" id="question4">
    <p>هل صبحي يعشق ريتاج؟</p>
    <button class="button" onclick="showQuestion('question5')">نعم</button>
    <button class="button" onclick="showQuestion('question5')">لا</button>
  </div>

  <div class="container hidden" id="question5">
    <p>أين يكون صبحي الساعة ١٢:٠٠؟</p>
    <button class="button" onclick="finishQuiz()">بالبيت نايم</button>
    <button class="button" onclick="finishQuiz()">طالع مع أصدقائه</button>
  </div>

  <!-- صفحة النهاية -->
  <div class="container hidden" id="finishPage">
    <h1>تم الإجابة!</h1>
    <p>اختر طريقة الإرسال:</p>
    <button class="button" onclick="copyResults()">نسخ الإجابات</button>
    <button class="button" onclick="openInstagram()">فتح حساب صبحي</button>
    <button class="button" onclick="shareResults()">مشاركة الإجابات</button>
  </div>

  <script>
    function goToPage2() {
      document.getElementById('page1').classList.add('hidden');
      document.getElementById('page2').classList.remove('hidden');
    }

    function showQuestion(nextId) {
      const currentVisible = document.querySelector('.container:not(.hidden)');
      currentVisible.classList.add('hidden');
      document.getElementById(nextId).classList.remove('hidden');
    }

    function finishQuiz() {
      const currentVisible = document.querySelector('.container:not(.hidden)');
      currentVisible.classList.add('hidden');
      document.getElementById('finishPage').classList.remove('hidden');
    }

    function copyResults() {
      const text = `إجابات ريتاج:\n١. ١٦\n٢. جميع ما سبق\n٣. لا\n٤. نعم\n٥. بالبيت نايم`;
      navigator.clipboard.writeText(text).then(() => {
        alert('تم نسخ الإجابات!');
      });
    }

    function openInstagram() {
      window.open("https://www.instagram.com/t.xil5/", "_blank");
    }

    function shareResults() {
      const text = `إجابات ريتاج:\n١. ١٦\n٢. جميع ما سبق\n٣. لا\n٤. نعم\n٥. بالبيت نايم`;
      if (navigator.share) {
        navigator.share({
          title: 'نتيجة اختبار ريتاج',
          text: text
        });
      } else {
        alert('مشاركة غير مدعومة على هذا الجهاز.');
      }
    }
  </script>

</body>
</html>