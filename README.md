
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
        .name-input {
            margin-top: 40px;
        }
        input[type="text"] {
            padding: 10px;
            font-size: 18px;
            border: 2px solid #d63384;
            border-radius: 8px;
            width: 200px;
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
        <h1 id="nameDisplay">ريتاج</h1>
        <h2>احبك واعشقك يا افضل من دخل قلبي وحياتي</h2>

        <div class="name-input">
            <p>غيّر الاسم:</p>
            <input type="text" id="nameInput" placeholder="اكتبي اسمك هنا">
            <button class="button" onclick="changeName()">مشاركة</button>
        </div>

        <div class="fixed-name">اسم الموقع محفوظ لـ: صبحي عبد الكريم</div>
    </div>

    <script>
        function startSite() {
            document.getElementById("welcomeScreen").style.display = "none";
            document.getElementById("mainContent").style.display = "block";
        }

        function changeName() {
            var newName = document.getElementById("nameInput").value.trim();
            if(newName !== "") {
                document.getElementById("nameDisplay").innerText = newName;
            }
        }
    </script>
</body>
</html>
