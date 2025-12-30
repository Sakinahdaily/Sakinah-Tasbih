<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>عداد التسبيح</title>

<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #fdf6e3;
    padding: 20px;
  }

  #count {
    font-size: 60px;
    color: #e74c3c;
    margin: 20px 0;
  }

  button {
    font-size: 22px;
    padding: 12px 25px;
    margin: 10px;
    border: none;
    border-radius: 10px;
    background-color: #3498db;
    color: white;
    cursor: pointer;
  }

  button:hover {
    background-color: #2980b9;
  }

  .readme {
    max-width: 600px;
    margin: 40px auto;
    background: white;
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    font-size: 18px;
    line-height: 1.8;
  }
</style>
</head>

<body>

<h1>📿 عداد التسبيح</h1>

<div id="count">0</div>

<button onclick="increment()">➕ إضافة 1</button>
<button onclick="resetCounter()">🔄 إعادة تعيين</button>

<div class="readme">
  <h2>📖 طريقة الاستخدام</h2>
  <p>هذا عدّاد بسيط للتسبيح والذكر.</p>
  <p>اضغط على زر <strong>إضافة 1</strong> لزيادة العدد.</p>
  <p>يتم حفظ العدد تلقائيًا حتى بعد إغلاق الصفحة.</p>
  <p>اضغط <strong>إعادة تعيين</strong> للبدء من جديد.</p>

  <p>
    قال رسول الله ﷺ:<br>
    <em>
      «كلمتان خفيفتان على اللسان، ثقيلتان في الميزان:
      سبحان الله وبحمده، سبحان الله العظيم»
    </em>
  </p>
</div>

<script>
let count = localStorage.getItem('tasbihCount')
  ? parseInt(localStorage.getItem('tasbihCount'))
  : 0;

document.getElementById('count').innerText = count;

function increment() {
  count++;
  document.getElementById('count').innerText = count;
  localStorage.setItem('tasbihCount', count);
}

function resetCounter() {
  count = 0;
  document.getElementById('count').innerText = count;
  localStorage.setItem('tasbihCount', count);
}
</script>

</body>
</html>
