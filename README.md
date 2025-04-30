<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>ريتاج(حب)صبحي</title>
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
      overflow-x: hidden;
    }

    .container {
      text-align: center;
      width: 100%;
      max-width: 400px;
      margin: auto;
      padding: 20px;
      box-sizing: border-box;
      animation: fadeInUp 1s ease-out forwards;
      opacity: 0;
    }

    h1 {
      font-size: 24px;
      color: #ffccff;
      margin-bottom: 10px;
    }

    p {
      font-size: 16px;
      color: #ffebcd;
      margin-bottom: 15px;
    }

    .button {
      background-color: #ff0066;
      color: white;
      padding: 12px;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin: 10px 0;
      width: 100%;
      max-width: 300px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
      display: block;
      transition: transform 0.2s ease;
    }

    .button:hover {
      transform: scale(1.05);
    }

    .hidden {
      display: none;
    }

    @keyframes fadeInUp {
      0% {
        opacity: 0;
        transform: translateY(20px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <div class="container" id="finishPage">
    <h1>تمت الإجابة على الأسئلة!</h1>
    <p>اختاري الطريقة المناسبة لمشاركة الإجابات مع صبحي:</p>

    <button class="button" onclick="sendToWhatsApp()">إرسال إلى واتساب</button>
    <button class="button" onclick="copyThenGoToInsta()">إرسال إلى انستغرام</button>
    <button class="button" onclick="shareResults()">مشاركة في أي تطبيق</button>
    <button class="button" onclick="copyResults()">نسخ النتائج</button>
  </div>

  <script>
    const answers = {
      age: "١٦",
      favoriteDish: "جميع ما سبق",
      prefersSugar: "لا يفضل ريتاج عن السكر لأنها هي السكر",
      lovesRetaj: "نعم",
      location: "بالبيت نايم"
    };

    const resultText = `إجابات الأسئلة:\n
١. كم عمر صبحي؟: ${answers.age}\n
٢. أفضل أكلة لدى صبحي؟: ${answers.favoriteDish}\n
٣. هل صبحي يفضل السكر على ريتاج؟: ${answers.prefersSugar}\n
٤. هل صبحي يعشق ريتاج؟: ${answers.lovesRetaj}\n
٥. أين يكون صبحي الساعة ١٢:٠٠؟: ${answers.location}`;

    function sendToWhatsApp() {
      const url = `https://wa.me/966557073705?text=${encodeURIComponent(resultText)}`;
      window.open(url, "_blank");
    }

    function copyResults() {
      navigator.clipboard.writeText(resultText).then(() => {
        alert("تم نسخ النتائج!");
      });
    }

    function copyThenGoToInsta() {
      navigator.clipboard.writeText(resultText).then(() => {
        window.open("https://instagram.com/t.xil5", "_blank");
      });
    }

    function shareResults() {
      if (navigator.share) {
        navigator.share({
          title: "إجابات صبحي",
          text: resultText
        }).catch((error) => console.error('Error sharing', error));
      } else {
        alert("جهازك لا يدعم المشاركة التلقائية");
      }
    }

    // لإظهار الصفحة مباشرة عند التحميل
    window.onload = () => {
      document.getElementById('finishPage').style.opacity = 1;
    };
  </script>
</body>
</html>