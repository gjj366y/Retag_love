<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>ريتاج</title>
    <style>
        body {
            background: linear-gradient(to bottom right, #ffe0ec, #fff5f9);
            font-family: 'Arial', sans-serif;
            text-align: center;
            padding: 50px;
            color: #d63384;
        }
        h1 {
            font-size: 48px;
            margin-bottom: 10px;
        }
        h2 {
            font-size: 24px;
            margin-top: 0;
        }
        .button {
            background-color: #d63384;
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 20px;
            border-radius: 10px;
            cursor: pointer;
            margin-top: 30px;
        }
        .button:hover {
            background-color: #c2185b;
        }
        textarea {
            margin-top: 30px;
            padding: 10px;
            font-size: 18px;
            border: 2px solid #d63384;
            border-radius: 8px;
            width: 80%;
            max-width: 400px;
            height: 100px;
            resize: none;
        }
        .fixed-name {
            margin-top: 50px;
            font-size: 16px;
            color: #999;
        }
        #mainContent {
            display: none;
        }
    </style>
</head>
<body>
    <div id="welcomeScreen">
        <button class="button" onclick="startSite()">اضغط هنا</button>
    </div>

    <div id="mainContent">
        <h1>ريتاج</h1>
        <h2>احبك واعشقك يا افضل من دخل قلبي وحياتي</h2>

        <div>
            <p>أرسل كلام إلى صبحي:</p>
            <textarea id="messageInput" placeholder="اكتب رسالتك هنا..."></textarea>
            <br>
            <button class="button" onclick="shareMessage()">مشاركة الكلام</button>
        </div>

        <div class="fixed-name">اسم الموقع محفوظ لـ: صبحي عبد الكريم</div>
    </div>

    <script>
        function startSite() {
            document.getElementById("welcomeScreen").style.display = "none";
            document.getElementById("mainContent").style.display = "block";
        }

        function shareMessage() {
            const message = document.getElementById("messageInput").value.trim();
            if (message) {
                if (navigator.share) {
                    navigator.share({
                        title: "رسالة إلى صبحي",
                        text: message
                    }).catch(console.error);
                } else {
                    alert("جهازك لا يدعم المشاركة التلقائية. انسخ الرسالة يدويًا.");
                }
            } else {
                alert("اكتب رسالة قبل المشاركة.");
            }
        }
    </script>
</body>
</html>