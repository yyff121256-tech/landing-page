<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>صفحة زواج VIP سهلة التعديل</title>

<style>
    body{
        margin:0;
        background:#f4f4f4;
        font-family:"Tahoma",sans-serif;
    }

    /* هيدر */
    header{
        padding:90px 20px;
        text-align:center;
        color:white;
        background:url('https://i.imgur.com/pCb9QaH.jpeg');
        background-size:cover;
        background-position:center;
        position:relative;
    }
    header::before{
        content:"";
        position:absolute;
        top:0; left:0;
        width:100%; height:100%;
        background:rgba(0,0,0,0.55);
    }
    header *{ position:relative; z-index:2; }

    header h1{
        font-size:38px;
        margin:0 0 15px;
        cursor:pointer;
    }
    header p{
        font-size:20px;
        cursor:pointer;
    }

    .section{
        background:white;
        padding:30px 20px;
        margin:20px;
        border-radius:12px;
        box-shadow:0 0 15px rgba(0,0,0,0.1);
        text-align:center;
    }
    h2,h3,p,li{ cursor:pointer; }

    ul{
        text-align:right;
        max-width:650px;
        margin:auto;
        font-size:18px;
        line-height:2;
    }

    /* نموذج */
    .form-box{
        max-width:650px;
        margin:auto;
        text-align:right;
    }
    .form-box input, .form-box textarea{
        width:100%;
        padding:12px;
        margin:8px 0;
        border:1px solid #bbb;
        border-radius:8px;
        font-size:17px;
    }

    .btn-send{
        background:#c2185b;
        color:white;
        padding:14px;
        width:100%;
        border:none;
        border-radius:8px;
        font-size:20px;
        cursor:pointer;
    }

    /* أزرار التواصل */
    .contact-buttons a{
        display:block;
        padding:15px;
        margin:10px 0;
        color:white;
        font-size:20px;
        border-radius:8px;
        text-decoration:none;
        font-weight:bold;
    }
    .wa{ background:#25D366; }
    .tg{ background:#0088cc; }
    .ph{ background:#111; }

    /* زر حفظ */
    #saveBtn{
        position:fixed;
        bottom:20px;
        left:20px;
        background:#111;
        color:white;
        padding:12px 20px;
        border-radius:10px;
        cursor:pointer;
        z-index:999;
        font-size:18px;
    }
</style>
</head>

<body>

<header>
    <h1 contenteditable="true" id="title">منصة الزواج والارتباط الشرعي</h1>
    <p contenteditable="true" id="subtitle">
        سجّل الآن واحصل على فرصة للتواصل مع شريك حياتك بكل خصوصية واحترام.
    </p>
</header>

<!-- قسم من نحن -->
<div class="section">
    <h2 contenteditable="true">من نحن</h2>
    <p contenteditable="true">
        نحن منصة متخصصة في التوفيق بين الراغبين بالزواج الشرعي بكل جدية واحترام وخصوصية،
        هدفنا مساعدتك في إيجاد شريك الحياة المناسب وفق معاييرك.
    </p>
</div>

<!-- الشروط -->
<div class="section">
    <h2 contenteditable="true">شروط التسجيل</h2>
    <ul>
        <li contenteditable="true">العمر 18 سنة وما فوق.</li>
        <li contenteditable="true">الجدية التامة في الزواج.</li>
        <li contenteditable="true">تقديم معلومات صحيحة وواضحة.</li>
        <li contenteditable="true">احترام خصوصية الآخرين.</li>
        <li contenteditable="true">عدم إرسال معلومات غير مناسبة.</li>
    </ul>
</div>

<!-- مميزات الخدمة -->
<div class="section">
    <h2 contenteditable="true">مميزات منصتنا</h2>
    <ul>
        <li contenteditable="true">خصوصية وسرية كاملة للبيانات.</li>
        <li contenteditable="true">سرعة في الرد والتواصل.</li>
        <li contenteditable="true">طلبات حقيقية وجادة.</li>
        <li contenteditable="true">إمكانية اختيار مواصفات الشريك بوضوح.</li>
        <li contenteditable="true">دعم على مدار الساعة.</li>
    </ul>
</div>

<!-- نموذج التسجيل -->
<div class="section" id="form">
    <h2 contenteditable="true">نموذج تسجيل طلب الزواج</h2>

    <div class="form-box">
        <input id="name" type="text" placeholder="الاسم الكامل">
        <input id="age" type="number" placeholder="العمر">
        <input id="country" type="text" placeholder="البلد / المنطقة">
        <input id="whatsapp" type="text" placeholder="رقم الواتساب">
        <textarea id="details" rows="4" placeholder="صف نفسك واذكر مواصفات الشريك المطلوب"></textarea>

        <button class="btn-send" onclick="sendData()">إرسال الطلب عبر واتساب</button>
    </div>
</div>

<script>
function sendData(){
    let name = document.getElementById("name").value;
    let age = document.getElementById("age").value;
    let country = document.getElementById("country").value;
    let whatsapp = document.getElementById("whatsapp").value;
    let details = document.getElementById("details").value;

    let msg = `طلب تسجيل زواج:%0A
الاسم: ${name}%0A
العمر: ${age}%0A
البلد: ${country}%0A
واتساب: ${whatsapp}%0A
التفاصيل: ${details}`;

    let admin = document.getElementById("mainNumber").innerText.trim();

    window.open(`https://wa.me/${admin}?text=${msg}`);
}
</script>

<!-- قسم التواصل -->
<div class="section">
    <h2 contenteditable="true">طرق التواصل</h2>

    <p contenteditable="true" id="mainNumber">0000000000</p>

    <div class="contact-buttons">
        <a id="waLink" class="wa" href="#" target="_blank">واتساب</a>
        <a id="tgLink" class="tg" href="#" target="_blank">تليجرام</a>
        <a id="phLink" class="ph" href="#">اتصال مباشر</a>
    </div>
</div>

<script>
// تحميل المحفوظ
window.onload=function(){
    document.querySelectorAll("[contenteditable]").forEach(el=>{
        let saved = localStorage.getItem(el.id);
        if(saved){ el.innerHTML = saved; }
    });
    updateLinks();
};

// حفظ
document.getElementById("saveBtn").onclick = function(){
    document.querySelectorAll("[contenteditable]").forEach(el=>{
        localStorage.setItem(el.id, el.innerHTML);
    });
    updateLinks();
    alert("✔ تم حفظ التعديلات");
};

function updateLinks(){
    let num = document.getElementById("mainNumber").innerText.trim();
    document.getElementById("waLink").href = "https://wa.me/" + num;
    document.getElementById("phLink").href = "tel:" + num;
    document.getElementById("tgLink").href = "https://t.me/username";
}
</script>

<!-- زر حفظ -->
<div id="saveBtn">💾 حفظ التعديلات</div>

</body>
</html>
