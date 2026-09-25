<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>دبیرستان محمدباقر مهدوی | پایگاه اطلاع‌رسانی</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css">
<style>
/* ========== محافظت ========== */
* {
  margin: 0; padding: 0; box-sizing: border-box;
  font-family: Tahoma, 'Segoe UI', sans-serif;
  -webkit-user-select: none; user-select: none;
}

/* ========== پس‌زمینه سایبرپانکی ========== */
:root {
  --cyan: #00F0FF;
  --blue-neon: #0088FF;
  --dark-bg: #050710;
  --card-bg: rgba(8, 15, 35, 0.85);
  --border-glow: rgba(0, 240, 255, 0.4);
  --text-primary: #E0F7FF;
  --text-secondary: #99CCFF;
  --accent-gold: #FFD700;
  --danger: #FF3366;
}

body {
  background: var(--dark-bg);
  background-image: 
    linear-gradient(rgba(0, 136, 255, 0.05) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0, 136, 255, 0.05) 1px, transparent 1px);
  background-size: 40px 40px;
  min-height: 100vh;
  color: var(--text-primary);
  line-height: 2;
  overflow-x: hidden;
}

.bg-glow {
  position: fixed; inset: 0; z-index: 0;
  background: 
    radial-gradient(circle at 20% 30%, rgba(0, 240, 255, 0.08) 0%, transparent 50%),
    radial-gradient(circle at 80% 70%, rgba(0, 136, 255, 0.1) 0%, transparent 50%);
  pointer-events: none;
}

/* ========== هدر ========== */
header {
  position: relative; z-index: 2;
  padding: 35px 20px;
  text-align: center;
  border-bottom: 1px solid var(--border-glow);
  background: linear-gradient(180deg, rgba(0, 40, 80, 0.8), rgba(5, 7, 16, 0.9));
  backdrop-filter: blur(10px);
}
.logo-text {
  font-size: 2rem; font-weight: 900;
  background: linear-gradient(90deg, var(--cyan), var(--blue-neon), var(--cyan));
  background-size: 200% auto;
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  animation: neonShine 3s linear infinite;
  text-shadow: 0 0 30px rgba(0, 240, 255, 0.3);
  letter-spacing: 1px;
}
@keyframes neonShine {
  to { background-position: 200% center; }
}
.subtitle {
  color: var(--text-secondary);
  margin-top: 10px; font-size: 15px;
  letter-spacing: 2px;
}

/* ========== ناوبری ========== */
nav {
  position: sticky; top: 0; z-index: 99;
  background: rgba(5, 7, 16, 0.9);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(0, 240, 255, 0.15);
  padding: 10px 0;
}
.nav-wrap {
  max-width: 1200px; margin: 0 auto; padding: 0 15px;
  display: flex; flex-wrap: wrap; justify-content: center; gap: 8px;
}
nav button {
  background: transparent; border: 1px solid transparent;
  padding: 12px 16px; color: var(--text-secondary);
  font-size: 14px; cursor: pointer; border-radius: 8px;
  transition: 0.3s;
}
nav button:hover {
  border-color: var(--cyan); color: var(--cyan);
  box-shadow: 0 0 15px rgba(0, 240, 255, 0.2);
}
nav button.active {
  background: linear-gradient(90deg, rgba(0, 240, 255, 0.15), rgba(0, 136, 255, 0.15));
  border-color: var(--cyan); color: var(--cyan);
  box-shadow: 0 0 20px rgba(0, 240, 255, 0.3), inset 0 0 10px rgba(0, 240, 255, 0.1);
}

/* ========== محتوا ========== */
.container {
  position: relative; z-index: 2;
  max-width: 1150px; margin: 30px auto; padding: 0 20px;
}
.page { display: none; animation: fadeIn 0.4s ease; }
.page.active { display: block; }
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(15px); }
  to { opacity: 1; transform: translateY(0); }
}

/* ========== کارت ========== */
.card {
  background: var(--card-bg);
  border: 1px solid var(--border-glow);
  border-radius: 16px; padding: 28px; margin-bottom: 25px;
  backdrop-filter: blur(8px);
  box-shadow: 0 0 20px rgba(0, 136, 255, 0.08);
  transition: 0.3s;
}
.card:hover {
  border-color: rgba(0, 240, 255, 0.5);
  box-shadow: 0 0 30px rgba(0, 240, 255, 0.15);
}
.card h2 {
  color: var(--cyan); font-size: 1.4rem; margin-bottom: 20px;
  padding-bottom: 10px; border-bottom: 1px solid rgba(0, 240, 255, 0.2);
  display: flex; align-items: center; gap: 10px;
}
.card h2 i { color: var(--blue-neon); }
.card h3 {
  color: var(--accent-gold); margin: 18px 0 10px; font-size: 1.1rem;
}
.card p {
  color: var(--text-primary); margin-bottom: 12px; font-size: 15px;
  text-align: justify;
}
.card strong { color: var(--cyan); }
.card hr {
  border: none; border-top: 1px dashed rgba(0, 240, 255, 0.2);
  margin: 25px 0;
}

/* ========== اطلاعیه ========== */
.notice {
  background: linear-gradient(135deg, rgba(0, 80, 150, 0.25), rgba(0, 40, 100, 0.25));
  border-left: 3px solid var(--cyan); border-radius: 10px;
  padding: 20px; margin-bottom: 18px;
}
.notice.warning {
  border-left-color: #FFD700; background: rgba(255, 215, 0, 0.08);
}
.notice.danger {
  border-left-color: var(--danger); background: rgba(255, 51, 102, 0.08);
}
.notice-title {
  font-weight: 900; font-size: 16px; margin-bottom: 10px;
  color: var(--cyan);
}
.notice.warning .notice-title { color: #FFD700; }
.notice.danger .notice-title { color: var(--danger); }
.date-tag {
  display: inline-block; background: rgba(0, 240, 255, 0.15);
  color: var(--cyan); padding: 4px 12px; border-radius: 20px;
  font-size: 12px; margin-bottom: 12px;
}

/* ========== لیست معلمان ========== */
.teacher-grid {
  display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 15px;
}
.teacher-card {
  background: rgba(0, 136, 255, 0.08);
  border: 1px solid rgba(0, 240, 255, 0.2);
  border-radius: 12px; padding: 18px;
  transition: 0.3s;
}
.teacher-card:hover {
  border-color: var(--cyan); transform: translateY(-3px);
  box-shadow: 0 5px 20px rgba(0, 240, 255, 0.15);
}
.teacher-name { font-weight: 900; color: var(--cyan); margin-bottom: 5px; }
.teacher-role { color: var(--text-secondary); font-size: 13px; margin-bottom: 10px; }
.teacher-id {
  display: inline-block; background: rgba(0, 240, 255, 0.1);
  color: var(--text-primary); padding: 5px 12px;
  border-radius: 6px; font-family: monospace; font-size: 13px;
}

/* ========== جدول ========== */
table {
  width: 100%; border-collapse: collapse; margin: 20px 0;
}
th, td {
  padding: 12px 10px; text-align: center;
  border: 1px solid rgba(0, 240, 255, 0.2);
}
th {
  background: rgba(0, 136, 255, 0.2); color: var(--cyan);
  font-weight: 900;
}
tr:nth-child(even) { background: rgba(0, 40, 100, 0.15); }

/* ========== دکمه مدیریت ========== */
.admin-float { position: fixed; top: 20px; left: 20px; z-index: 100; }
.admin-btn {
  width: 55px; height: 55px; border-radius: 50%; border: none;
  background: linear-gradient(90deg, var(--cyan), var(--blue-neon));
  font-size: 22px; cursor: pointer;
  box-shadow: 0 0 25px rgba(0, 240, 255, 0.4);
  transition: 0.3s; display: none;
}
.admin-btn:hover { transform: scale(1.15); }

/* ========== مودال ========== */
.modal {
  position: fixed; inset: 0; background: rgba(0, 5, 15, 0.92);
  display: none; align-items: center; justify-content: center;
  padding: 20px; z-index: 200;
}
.modal.show { display: flex; }
.modal-box {
  background: var(--card-bg); border: 2px solid var(--cyan);
  border-radius: 16px; padding: 30px;
  width: 100%; max-width: 450px;
  box-shadow: 0 0 40px rgba(0, 240, 255, 0.2);
}
.modal-title { color: var(--cyan); margin-bottom: 20px; text-align: center; font-size: 1.3rem; }
input, textarea {
  width: 100%; padding: 14px; border-radius: 8px;
  border: 1px solid var(--border-glow);
  background: rgba(0, 20, 40, 0.8);
  color: var(--text-primary); margin: 8px 0; font-size: 14px;
}
.btn {
  width: 100%; padding: 14px; border-radius: 8px; border: none;
  font-size: 15px; font-weight: 900; cursor: pointer;
  margin-top: 10px; transition: 0.2s;
}
.btn-cyan { background: linear-gradient(90deg, var(--cyan), var(--blue-neon)); color: #000; }
.btn-dark { background: rgba(0, 40, 80, 0.5); color: var(--text-secondary); border: 1px solid rgba(0, 240, 255, 0.2); }
.btn:hover { transform: scale(1.03); }

/* ========== فوتر ========== */
footer {
  position: relative; z-index: 2;
  border-top: 1px solid var(--border-glow);
  padding: 30px 20px; text-align: center;
  color: var(--text-secondary); font-size: 13px;
  margin-top: 60px;
}
</style>
</head>
<body oncontextmenu="return false;">

<div class="bg-glow"></div>

<!-- دکمه مدیریت -->
<div class="admin-float">
  <button class="admin-btn" id="adminToggle" onclick="openLogin()">⚙️</button>
</div>

<!-- هدر -->
<header>
  <h1 class="logo-text">🏫 دبیرستان محمدباقر مهدوی</h1>
  <p class="subtitle">پایگاه اطلاع‌رسانی و آموزشی — خوانسار</p>
</header>

<!-- ناوبری -->
<nav>
  <div class="nav-wrap">
    <button class="active" onclick="showPage('home')">خانه</button>
    <button onclick="showPage('messages')">پیام‌های مدیریت</button>
    <button onclick="showPage('rules')">قوانین و مقررات</button>
    <button onclick="showPage('schedule')">برنامه کلاسی</button>
    <button onclick="showPage('teachers')">معلمان</button>
    <button onclick="showPage('contact')">تماس و ارتباط</button>
  </div>
</nav>

<!-- محتوای اصلی -->
<main class="container">

  <!-- صفحه خانه -->
  <div class="page active" id="page-home">
    <div class="card">
      <h2><i class="fas fa-bullhorn"></i> آخرین اطلاعیه‌ها</h2>
      
      <div class="notice warning">
        <div class="notice-title">⚠️ اطلاعیه — لباس فرم</div>
        <p>با توجه به تماس والدین محترم در خصوص لباس فرم دانش‌آموزان در سال تحصیلی جدید، لازم به ذکر است:</p>
        <p>✅ لباس فرم برای متوسطه اول الزامی نبوده و مدرسه مهدوی برای سال تحصیلی جدید لباس فرم در نظر نگرفته است.</p>
        <p>✅ دانش‌آموزان با لباس معمول و طبق ضوابط آموزش و پرورش در مدرسه حضور پیدا کنند.</p>
      </div>

      <div class="notice danger">
        <div class="notice-title">❗️ شروع کلاس‌ها — اول مهرماه</div>
        <p>چهارشنبه اول مهرماه مدرسه دایر و برنامه کلاسی طبق برنامه ارسالی در کانال می‌باشد.</p>
        <p><strong>عدم حضور به منزله غیبت غیرمجاز است 🚫</strong></p>
        <p>⏰ ساعت صبحگاه: راس ساعت ۸ صبح — قبل از ۸ در مدرسه حاضر باشید.</p>
        <p>بعد از زنگ صبحگاه، تاخیر طبق مقررات رفتار خواهد شد.</p>
      </div>
    </div>
  </div>

  <!-- پیام‌های مدیریت -->
  <div class="page" id="page-messages">
    <div class="card">
      <h2><i class="fas fa-scroll"></i> پیام تقدیر و خداحافظی — جناب آقای سمیعیانی</h2>
      
      <p><strong>بسم‌الله الرحمن الرحیم</strong></p>
      <p>با سلام و احترام</p>
      
      <p>پس از دو سال همراهی و خدمت در دبیرستان محمدباقر مهدوی، اکنون با واگذاری مسئولیت مدیریت مدرسه، فرصت خداحافظی با مجموعه‌ای ارزشمند و خاطره‌انگیز برای بنده فرا رسیده است.</p>
      
      <p>در این مدت، همراهی، اعتماد و همکاری صمیمانه همکاران گرامی، دانش‌آموزان عزیز و خانواده‌های محترم، همواره پشتوانه‌ای ارزشمند برای اینجانب بوده و از همه عزیزانی که در مسیر پیشبرد امور مدرسه و تحقق اهداف آموزشی و تربیتی یاری‌رسان بودند، صمیمانه سپاسگزارم.</p>
      
      <p>لازم می‌دانم از اعضای محترم انجمن مدرسه نیز صمیمانه قدردانی کنم که با همراهی، همفکری، دلسوزی و حمایت‌های ارزشمند خود، در طول این دو سال در کنار مدیریت مدرسه بودند و در مسیر بهبود امور و پیشرفت مجموعه، نقش مؤثری ایفا کردند. بی‌تردید همراهی و اعتماد اعضای محترم انجمن، از سرمایه‌های ارزشمند این دوران بود و از زحمات و همکاری‌های صمیمانه آنان سپاسگزارم.</p>
      
      <p>خوشحالم که در کنار شما عزیزان، بخشی از مسیر رشد و پیشرفت این مجموعه را طی کردم و خاطرات این دو سال را با خود به یادگار خواهم داشت.</p>
      
      <p>در پایان، برای جناب آقای سامان موحد، مدیر جدید دبیرستان محمدباقر مهدوی، آرزوی توفیق و سربلندی دارم و امیدوارم با تلاش، انگیزه و همراهی همه همکاران، انجمن محترم مدرسه، دانش‌آموزان و خانواده‌های گرامی، شاهد تداوم موفقیت‌ها و پیشرفت روزافزون این مدرسه باشیم.</p>
      
      <p>از همه شما عزیزان بابت محبت‌ها، همراهی‌ها، اعتماد و خاطرات ارزشمند این دوران صمیمانه سپاسگزارم.</p>
      
      <p style="text-align: left; margin-top: 25px; color: var(--accent-gold);">با احترام<br>✍️ مسعود سمیعیانی</p>
      
      <hr>
      
      <h2><i class="fas fa-handshake"></i> پیام تبریک و خوشآمدگویی — جناب آقای موحد</h2>
      
      <p><strong>بسم‌الله الرحمن الرحیم</strong></p>
      
      <p>همکار ارجمند جناب آقای مسعود سمیعیانی</p>
      
      <p>با سلام و احترام فراوان، از جنابعالی بابت دو سال خدمت در جایگاه مدیریت مدرسه مهدوی و تلاش شما برای اعتلای علم و فرهنگ دانش‌آموزان خوانسار عزیز و ارتقای سطح کیفی مدرسه، صمیمانه سپاسگزاری کرده و از خداوند متعال موفقیت روزافزون و هرچه بیشتر حضرتعالی را در سمت والای معلمی خواستارم.</p>
      
      <p style="text-align: left; margin-top: 20px; color: var(--accent-gold);">با تقدیم ادب و احترام<br>سامان موحد</p>
    </div>
  </div>

  <!-- قوانین و مقررات -->
  <div class="page" id="page-rules">
    <div class="card">
      <h2><i class="fas fa-book"></i> قوانین و مقررات مدرسه</h2>
      
      <h3>لباس و ظاهر</h3>
      <ul style="margin: 10px 0 20px 25px;">
        <li>✅ لباس باید معمول، مرسوم و ساده باشد</li>
        <li>❌ آستین کوتاه — ممنوع</li>
        <li>❌ لباس و شلوار تنگ و چسبان — ممنوع</li>
        <li>❌ شلوار زاپ‌دار — ممنوع</li>
        <li>❌ شلوار راحتی — ممنوع</li>
        <li>در صورت رعایت نکردن، از ورود به کلاس جلوگیری خواهد شد.</li>
      </ul>
      
      <h3>وسایل شخصی</h3>
      <ul style="margin: 10px 0 20px 25px;">
        <li>❌ تلفن همراه — ممنوع است</li>
        <li>❌ وسایل زینتی (گردنبند و ...) — ممنوع</li>
        <li>❌ فندک، پنجه‌بکس و وسایل غیرمعمول — ممنوع و ضبط می‌شود</li>
      </ul>
      
      <h3>حفاظت از اموال مدرسه</h3>
      <p>در صورت آسیب رساندن به اموال عمومی شامل: صندلی‌ها، وسایل آموزشی، شیرآلات، تجهیزات گرمایش، آزمایشگاه، کتابخانه، درب‌ها، دیوارها، کف سالن، حیاط و ... ضمن دریافت خسارت و جریمه، با متخلف طبق مقررات برخورد خواهد شد.</p>
      
      <h3>رفتار و گفتار</h3>
      <div class="notice danger">
        <p><strong>⚠️ مهم:</strong> فحاشی و استفاده از الفاظ رکیک در قانون جمهوری اسلامی ایران جرم محسوب می‌شود و موجب جزای نقدی و حتی شلاق است.</p>
        <p>در محیط مدرسه، چنانچه توسط دبیران و کادر اجرایی مشاهده یا به صورت مستند اثبات شود، شدیداً برخورد خواهد شد.</p>
      </div>
      
      <h3>گزارش مشکلات</h3>
      <p>اولیای محترم می‌توانند هرگونه مشکل دانش‌آموز شامل موارد زیر را به صورت محرمانه در میان بگذارند:</p>
      <ul style="margin: 10px 0 20px 25px;">
        <li>مشکلات جسمانی: قلبی، تنفسی، گفتاری، حرکتی، دیداری، شنیداری، کلیوی و ...</li>
        <li>مشکلات روحی: انزوا، استرس، اضطراب، آسیب‌های عاطفی و ...</li>
        <li>مشکلات ذهنی: عدم تمرکز، فراموشی، ضعف یادگیری و ...</li>
      </ul>
      <p>📞 با <strong>آقای طالاری</strong> (مشاور مدرسه) در روزهای شنبه — حضوری</p>
      <p>📞 با مدیر مدرسه — حضوری یا از طریق آیدی: <strong>@saman68kh</strong></p>
    </div>
  </div>

  <!-- برنامه کلاسی -->
  <div class="page" id="page-schedule">
    <div class="card">
      <h2><i class="fas fa-clock"></i> ساعت‌های حضور</h2>
      
      <table>
        <tr><th>بخش</th><th>ساعت</th></tr>
        <tr><td>حضور در مدرسه</td><td>۷:۳۰ الی ۷:۴۵</td></tr>
        <tr><td>برنامه صبحگاه</td><td>۷:۴۵ الی ۸:۰۰</td></tr>
        <tr><td>پایان کلاس‌ها</td><td>۱۳:۰۰</td></tr>
      </table>
      
      <p style="margin-top: 20px;">نماز فضیلت هر روزه به اطلاع کلاس مربوطه خواهد رسید.</p>
    </div>
  </div>

  <!-- معلمان -->
  <div class="page" id="page-teachers">
    <div class="card">
      <h2><i class="fas fa-chalkboard-teacher"></i> راه ارتباطی با دبیران</h2>
      
      <div class="teacher-grid">
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای طالاری</div>
          <div class="teacher-role">مشاور مدرسه</div>
          <div class="teacher-id">@mohamadtlri</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای قشونی</div>
          <div class="teacher-role">مربی پرورشی</div>
          <div class="teacher-id">@ghoshoni76</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای مدرسی</div>
          <div class="teacher-role">دبیر ریاضی</div>
          <div class="teacher-id">@m12726</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای رضایت</div>
          <div class="teacher-role">دبیر علوم تجربی</div>
          <div class="teacher-id">@Mohsen_rezayat</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای عمادی</div>
          <div class="teacher-role">دبیر زبان انگلیسی</div>
          <div class="teacher-id">@AminEmadii</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای خسروی</div>
          <div class="teacher-role">دبیر ورزش</div>
          <div class="teacher-id">@Morteza_PhDStudent</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای یگانه</div>
          <div class="teacher-role">دبیر مطالعات اجتماعی</div>
          <div class="teacher-id">@mr_yegane1</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای حمراطلایی</div>
          <div class="teacher-role">دبیر قرآن و معارف</div>
          <div class="teacher-id">@Talaei29</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای سلامی</div>
          <div class="teacher-role">دبیر ادبیات فارسی</div>
          <div class="teacher-id">@Hasan_Salami</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای خسروی</div>
          <div class="teacher-role">دبیر کار و فناوری</div>
          <div class="teacher-id">@amirhkh80</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای مرادی</div>
          <div class="teacher-role">دبیر نگارش</div>
          <div class="teacher-id">@Mehran_m</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای منصوری</div>
          <div class="teacher-role">دبیر عربی</div>
          <div class="teacher-id">@Mansouri3133</div>
        </div>
        
        <div class="teacher-card">
          <div class="teacher-name">جناب آقای ایرانی</div>
          <div class="teacher-role">دبیر هنر</div>
          <div class="teacher-id">—</div>
        </div>
      </div>
    </div>
  </div>

  <!-- تماس با ما -->
  <div class="page" id="page-contact">
    <div class="card">
      <h2><i class="fas fa-address-card"></i> تماس با ما</h2>
      
      <p><strong>📍 آدرس:</strong> خوانسار — دبیرستان محمدباقر مهدوی</p>
      <p><strong>📱 ارتباط با مدیر:</strong> @saman68kh</p>
      <p><strong>🕐 ساعات کاری:</strong> ۷:۳۰ الی ۱۳:۰۰</p>
      <p style="margin-top: 20px; color: var(--accent-gold);">با تشکر از همراهی شما 🙏</p>
    </div>
  </div>

</main>

<!-- فوتر -->
<footer>
  <p>© ۱۴۰۴ — دبیرستان محمدباقر مهدوی | خوانسار | تمامی حقوق محفوظ است</p>
</footer>

<!-- پنل ورود مدیریت -->
<div class="modal" id="loginModal">
  <div class="modal-box">
    <h3 class="modal-title">🔐 ورود به مدیریت</h3>
    <input type="password" id="passInput" placeholder="رمز عبور را وارد کنید">
    <button class="btn btn-cyan" onclick="checkPass()">ورود</button>
    <button class="btn btn-dark" onclick="closeModal('loginModal')">بستن</button>
  </div>
</div>

<script>
// ⚙️ تنظیمات
const ADMIN_PASS = "123456"; // رمز مدیریت

let isAdmin = false;

// ========== نمایش صفحه ==========
function showPage(id) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('nav button').forEach(b => b.classList.remove('active'));
  document.getElementById(`page-${id}`).classList.add('active');
  event.target.classList.add('active');
}

// ========== مدیریت ==========
function openLogin() { document.getElementById('loginModal').classList.add('show'); }
function closeModal(id) { document.getElementById(id).classList.remove('show'); }

function checkPass() {
  if (document.getElementById('passInput').value === ADMIN_PASS) {
    isAdmin = true;
    document.getElementById('adminToggle').style.display = 'block';
    closeModal('loginModal');
    alert("✅ خوش آمدید! شما وارد پنل مدیریت شدید.");
  } else {
    alert("❌ رمز عبور اشتباه است!");
  }
}
</script>

</body>
</html>
