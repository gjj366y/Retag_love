<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>ريتاج - حب أبدي</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(120deg, #ffdee9, #b5fffc);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      color: #fff;
    }

    .container {
      text-align: center;
      z-index: 2;
      animation: fadeInUp 1s ease-out forwards;
      opacity: 0;
      text-shadow: 0 0 15px rgba(255, 255, 255, 0.8);
    }

    h1 {
      font-size: 56px;
      margin-bottom: 20px;
      animation-delay: 0.5s;
      color: #ffccff;
    }

    p {
      font-size: 28px;
      animation-delay: 1.2s;
      line-height: 1.5;
      color: #ffebcd;
    }

    .signature {
      margin-top: 40px;
      font-size: 20px;
      color: #fff;
      opacity: 0.7;
      animation-delay: 2s;
      font-style: italic;
    }

    .button {
      background-color: rgba(255, 255, 255, 0.4);
      color: white;
      padding: 15px 30px;
      font-size: 22px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin: 20px 0;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s ease;
    }

    .button:hover {
      transform: scale(1.1);
    }

    .hidden {
      display: none;
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
  </style>
</head>
<body>

  <div class="container">
    <h1>أهلاً ياعمري ياريتاج</h1>
    <p>أنتِ نبضي، وهدوء روحي، وكل لحظة حلوة في حياتي.</p>
    <button class="button" id="firstButton">اضغطي هنا ياروحي</button>

    <!-- Hidden messages -->
    <div class="message hidden" id="messageOne">
      <p>أنتِ جميلة في كل لحظة، وجودك يجعل العالم أفضل.</p>
      <button class="button" id="secondButton">اضغطي هنا ياروحي</button>
    </div>

    <div class="message hidden" id="messageTwo">
      <p>شاركي الرابط باسم غير ريتاج:</p>
      <input type="text" id="customName" placeholder="اكتب اسمك هنا" />
      <button class="button" id="thirdButton">شارك الرابط</button>
    </div>

    <div class="message hidden" id="messageThree">
      <p>شاركي كلام حلو لحبيبك صبحي</p>
      <button class="button" id="finalButton">أرسل</button>
    </div>

    <!-- New buttons for sending to WhatsApp and Instagram -->
    <div class="message hidden" id="sendMessage">
      <button class="button" onclick="sendToWhatsApp()">إرسال إلى صبحي على واتساب</button>
      <button class="button" onclick="sendToInstagram()">إرسال إلى صبحي على إنستغرام</button>
    </div>

  </div>

  <script>
    // Buttons and message logic
    const firstButton = document.getElementById("firstButton");
    const secondButton = document.getElementById("secondButton");
    const thirdButton = document.getElementById("thirdButton");
    const finalButton = document.getElementById("finalButton");

    const messageOne = document.getElementById("messageOne");
    const messageTwo = document.getElementById("messageTwo");
    const messageThree = document.getElementById("messageThree");
    const sendMessage = document.getElementById("sendMessage");

    firstButton.addEventListener("click", () => {
      messageOne.classList.remove("hidden");
    });

    secondButton.addEventListener("click", () => {
      messageTwo.classList.remove("hidden");
    });

    thirdButton.addEventListener("click", () => {
      messageThree.classList.remove("hidden");
    });

    finalButton.addEventListener("click", () => {
      const customName = document.getElementById("customName").value;
      if (customName) {
        alert(`تم إرسال الرابط! تحياتي لـ ${customName}`);
        sendMessage.classList.remove("hidden"); // Show send message buttons
      }
    });

    // Send message functions
    function sendToWhatsApp() {
      const message = "أرسل رسالتك هنا!"; // يمكنك تعديل الرسالة
      const phoneNumber = "0557073705"; // رقم صبحي على واتساب
      window.open(`https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`, '_blank');
    }

    function sendToInstagram() {
      const username = "t.xil5"; // اسم المستخدم في إنستغرام
      const message = "أرسل رسالتك هنا!"; // يمكنك تعديل الرسالة
      window.open(`https://www.instagram.com/direct/t/${username}?text=${encodeURIComponent(message)}`, '_blank');
    }
  </script>

</body>
</html> 