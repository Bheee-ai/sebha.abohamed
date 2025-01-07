# sebha.abohamed
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>صدقة جارية للمرحوم الحبيب محمد أحمد حامد زيادة</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background-image: url('background.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: #fff;
            text-align: center;
        }

        .overlay {
            background: rgba(0, 0, 0, 0.6);
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }

        .content {
            position: relative;
            z-index: 2;
            padding: 20px;
        }

        .tasbeeh, .prayer {
            background: rgba(255, 255, 255, 0.2);
            padding: 15px;
            border-radius: 10px;
            margin: 20px auto;
            width: 80%;
            max-width: 600px;
            color: #fff;
        }

        footer {
            position: fixed;
            bottom: 0;
            width: 100%;
            background: rgba(0, 0, 0, 0.7);
            color: #fff;
            text-align: center;
            padding: 10px 0;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <audio autoplay loop>
        <source src="dua.mp3" type="audio/mp3">
        متصفحك لا يدعم الصوت.
    </audio>

    <div class="overlay"></div>
    <div class="content">
        <h1>صدقة جارية</h1>
        <div class="tasbeeh">
            <h2>عداد التسبيح</h2>
            <p>قم باختيار التسبيح:</p>
            <button onclick="tasbeeh('سبحان الله')">سبحان الله</button>
            <button onclick="tasbeeh('الحمد لله')">الحمد لله</button>
            <button onclick="tasbeeh('الله أكبر')">الله أكبر</button>
            <button onclick="tasbeeh('لا إله إلا الله')">لا إله إلا الله</button>
            <p>التسبيح الحالي: <span id="current-tasbeeh">--</span></p>
            <p>العدد: <span id="count">0</span></p>
            <button onclick="resetCounter()">تصفير العداد</button>
        </div>

        <div class="prayer">
            <h2>دعاء للمتوفي</h2>
            <p>اللهم ارحمه واغفر له، واجعل قبره روضة من رياض الجنة.</p>
            <p>اللهم اجعل عمله الصالح شفيعًا له يوم القيامة.</p>
            <p>اللهم تجاوز عن سيئاته وضاعف حسناته.</p>
        </div>
    </div>

    <footer>
        <p>© صمم الموقع بواسطة محبك في الله: باسم حماده</p>
    </footer>

    <script>
        let count = 0;

        function tasbeeh(type) {
            document.getElementById("current-tasbeeh").textContent = type;
            count++;
            document.getElementById("count").textContent = count;
        }

        function resetCounter() {
            count = 0;
            document.getElementById("count").textContent = count;
            document.getElementById("current-tasbeeh").textContent = "--";
        }
    </script>
</body>
</html>
صدقة جارية 
