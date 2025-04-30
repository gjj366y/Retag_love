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
      overflow: hidden;
      background: linear-gradient(120deg, #ffdee9, #b5fffc);
      height: 100vh;
      position: relative;
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 8s infinite ease-in;
      opacity: 0.6;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(45deg);
      }
      100% {
        transform: translateY(-10vh) rotate(45deg);
      }
    }

    .container {
      position: relative;
      z-index: 2;
      text-align: center;
      top: 50%;
      transform: translateY(-50%);
      padding: 20px;
      color: #fff;
    }

    h1, p {
      animation: fadeInUp 1s ease forwards;
      opacity: 0;
    }

    h1 {
      font-size: 48px;
      margin-bottom: 10px;
      animation-delay: 0.5s;
    }

    p {
      font-size: 24px;
      animation-delay: 1.2s;
    }

    .signature {
      margin-top: 40px;
      font-size: 16px;
      color: #fff;
      opacity: 0.7;
      animation-delay: 2s;
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

  <!-- قلوب تطير -->
  <div class="heart" style="left:10%; animation-duration: 7s;"></div>
  <div class="heart" style="left:30%; animation-duration: 9s;"></div>
  <div class="heart" style="left:50%; animation-duration: 6s;"></div>
  <div class="heart" style="left:70%; animation-duration: 8s;"></div>
  <div class="heart" style="left:90%; animation-duration: 7.5s;"></div>

  <div class="container">
    <h1>ريتاج</h1>
    <p>أنتِ نبضي، وهدوء روحي، وكل لحظة حلوة في حياتي.</p>
    <p>أحبك بكل تفاصيلك، يا من زينتِ عالمي بوجودك.</p>
    <div class="signature">— صبحي عبد الكريم</div>
  </div>

</body>
</html>