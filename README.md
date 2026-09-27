<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مدرسه پسرانه مهدوی | سامانه جامع قوانین و مقررات</title>
    <!-- فونت وزیرمتن -->
    <link href="https://cdn.jsdelivr.net/gh/rastikerdar/vazirmatn@v33.003/Vazirmatn-font-face.css" rel="stylesheet" type="text/css" />
    <!-- آیکون‌ها -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #0f4c75;
            --secondary: #3282b8;
            --accent: #bbe1fa;
            --dark: #1b262c;
            --light: #f0f5f9;
            --glass: rgba(255, 255, 255, 0.85);
            --glass-border: rgba(255, 255, 255, 0.3);
            --shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.15);
            --gradient: linear-gradient(135deg, #0f4c75 0%, #3282b8 100%);
            --radius: 16px;
            --transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            outline: none;
        }

        body {
            font-family: 'Vazirmatn', sans-serif;
            background-color: #eef2f5;
            color: var(--dark);
            overflow-x: hidden;
            line-height: 1.8;
        }

        /* اسکرول بار سفارشی */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: var(--light); }
        ::-webkit-scrollbar-thumb { background: var(--secondary); border-radius: 10px; }

        /* --- HEADER & NAVIGATION --- */
        header {
            background: var(--gradient);
            color: white;
            padding: 0;
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0,0,0,0.2);
            z-index: 100;
        }

        .header-bg-pattern {
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background-image: radial-gradient(circle at 20% 20%, rgba(255,255,255,0.1) 0%, transparent 20%),
                              radial-gradient(circle at 80% 80%, rgba(255,255,255,0.1) 0%, transparent 20%);
            opacity: 0.6;
            pointer-events: none;
        }

        .top-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-box {
            width: 60px;
            height: 60px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            color: var(--primary);
            box-shadow: 0 0 15px rgba(255,255,255,0.5);
            animation: pulse 3s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(255,255,255, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(255,255,255, 0); }
            100% { box-shadow: 0 0 0 0 rgba(255,255,255, 0); }
        }

        .school-name h1 { font-size: 1.8rem; font-weight: 900; letter-spacing: -0.5px; }
        .school-name span { font-size: 0.9rem; opacity: 0.9; font-weight: 300; }

        .nav-toggle {
            display: none;
            font-size: 24px;
            cursor: pointer;
            color: white;
        }

        /* --- LAYOUT GRID --- */
        .main-layout {
            display: grid;
            grid-template-columns: 280px 1fr;
            min-height: calc(100vh - 100px);
            max-width: 1600px;
            margin: 0 auto;
        }

        /* --- SIDEBAR --- */
        .sidebar {
            background: white;
            padding: 30px 20px;
            border-left: 1px solid #ddd;
            position: sticky;
            top: 0;
            height: 100vh;
            overflow-y: auto;
            box-shadow: 5px 0 15px rgba(0,0,0,0.05);
            z-index: 90;
        }

        .sidebar-title {
            font-size: 1.1rem;
            color: var(--primary);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--accent);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .menu-list { list-style: none; }
        
        .menu-item {
            margin-bottom: 8px;
        }

        .menu-link {
            display: flex;
            align-items: center;
            padding: 12px 15px;
            color: #555;
            text-decoration: none;
            border-radius: 10px;
            transition: var(--transition);
            font-size: 0.95rem;
            cursor: pointer;
        }

        .menu-link i { margin-left: 10px; width: 20px; text-align: center; color: var(--secondary); }

        .menu-link:hover, .menu-link.active {
            background: var(--light);
            color: var(--primary);
            transform: translateX(-5px);
            font-weight: bold;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .menu-link.active {
            background: var(--gradient);
            color: white;
        }
        .menu-link.active i { color: white; }

        /* --- CONTENT AREA --- */
        .content-area {
            padding: 40px;
            background: #f4f7fa;
        }

        .section {
            display: none;
            animation: slideUp 0.5s ease forwards;
        }

        .section.active { display: block; }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* --- CARDS & GLASSMORPHISM --- */
        .glass-card {
            background: var(--glass);
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass-border);
            border-radius: var(--radius);
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }

        .glass-card::before {
            content: '';
            position: absolute;
            top: 0; right: 0; width: 5px; height: 100%;
            background: var(--gradient);
        }

        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            border-bottom: 1px dashed #ccc;
            padding-bottom: 15px;
        }

        .card-title {
            font-size: 1.4rem;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* --- ACCORDION FOR RULES --- */
        .accordion {
            margin-top: 15px;
        }

        .acc-item {
            background: white;
            border-radius: 10px;
            margin-bottom: 10px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            border: 1px solid #eee;
        }

        .acc-header {
            padding: 18px 25px;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: bold;
            color: var(--dark);
            transition: var(--transition);
            background: white;
        }

        .acc-header:hover { background: #f8fbff; color: var(--secondary); }

        .acc-body {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s ease-out;
            background: #fafafa;
            border-top: 1px solid #eee;
        }

        .acc-content { padding: 25px; color: #444; font-size: 0.95rem; }

        .acc-icon { transition: transform 0.3s; }
        .acc-item.open .acc-icon { transform: rotate(180deg); }
        .acc-item.open .acc-header { background: var(--light); color: var(--primary); }

        /* --- SPECIFIC ELEMENTS --- */
        .badge {
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
        }
        .bg-red { background: #ffebee; color: #c62828; }
        .bg-green { background: #e8f5e9; color: #2e7d32; }
        .bg-blue { background: #e3f2fd; color: #1565c0; }

        .alert-box {
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
            display: flex;
            gap: 15px;
            align-items: start;
        }
        .alert-danger { background: #fff5f5; border-right: 4px solid #e53e3e; color: #9b2c2c; }
        .alert-info { background: #ebf8ff; border-right: 4px solid #3182ce; color: #2c5282; }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: white;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: var(--transition);
        }
        .stat-card:hover { transform: translateY(-5px); }
        .stat-number { font-size: 2.5rem; font-weight: 900; color: var(--secondary); display: block; }
        .stat-label { color: #777; font-size: 0.9rem; }

        /* TABLE STYLES */
        .table-container { overflow-x: auto; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.05); }
        table { width: 100%; border-collapse: collapse; background: white; }
        th, td { padding: 15px; text-align: right; border-bottom: 1px solid #eee; }
        th { background: var(--primary); color: white; font-weight: normal; }
        tr:hover { background: #f9f9f9; }

        /* RESPONSIVE */
        @media (max-width: 992px) {
            .main-layout { grid-template-columns: 1fr; }
            .sidebar { 
                position: fixed; 
                right: -300px; 
                top: 0; 
                height: 100%; 
                width: 280px; 
                transition: 0.3s;
                box-shadow: -5px 0 15px rgba(0,0,0,0.1);
            }
            .sidebar.show { right: 0; }
            .nav-toggle { display: block; }
            .content-area { padding: 20px; }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="header-bg-pattern"></div>
        <div class="top-bar">
            <div class="brand">
                <div class="logo-box"><i class="fas fa-graduation-cap"></i></div>
                <div class="school-name">
                    <h1>دبیرستان پسرانه مهدوی</h1>
                    <span>سامانه جامع قوانین، مقررات و اطلاع‌رسانی (پایه‌های ۷، ۸ و ۹)</span>
                </div>
            </div>
            <div class="nav-toggle" onclick="toggleSidebar()">
                <i class="fas fa-bars"></i>
            </div>
            <div style="display: flex; gap: 15px;">
                <button onclick="window.print()" style="background:rgba(255,255,255,0.2); border:none; color:white; padding:8px 15px; border-radius:8px; cursor:pointer;"><i class="fas fa-print"></i> چاپ قوانین</button>
            </div>
        </div>
    </header>

    <div class="main-layout">
        <!-- Sidebar Navigation -->
        <aside class="sidebar" id="sidebar">
            <div class="sidebar-title">
                <i class="fas fa-list-ul"></i> فهرست دسترسی سریع
            </div>
            <ul class="menu-list">
                <li class="menu-item"><a class="menu-link active" onclick="showSection('home', this)"><i class="fas fa-home"></i> داشبورد اصلی</a></li>
                <li class="menu-item"><a class="menu-link" onclick="showSection('appearance', this)"><i class="fas fa-tshirt"></i> پوشش و ظاهر</a></li>
                <li class="menu-item"><a class="menu-link" onclick="showSection('time', this)"><i class="fas fa-clock"></i> نظم و زمان‌بندی</a></li>
                <li class="menu-item"><a class="menu-link" onclick="showSection('classroom', this)"><i class="fas fa-chalkboard-teacher"></i> قوانین کلاس درس</a></li>
                <li class="menu-item"><a class="menu-link" onclick="showSection('exam', this)"><i class="fas fa-file-alt"></i> امتحانات و نمرات</a></li>
                <li class="menu-item"><a class="menu-link" onclick="showSection('tech', this)"><i class="fas fa-mobile-alt"></i> فناوری و موبایل</a></li>
                <li class="menu-item"><a class="menu-link" onclick="showSection('facilities', this)"><i class="fas fa-flask"></i> آزمایشگاه و کارگاه</a></li>
                <li class="menu-item"><a class="menu-link" onclick="showSection('camp', this)"><i class="fas fa-bus"></i> اردوها و بازدیدها</a></li>
                <li class="menu-item"><a class="menu-link" onclick="showSection('finance', this)"><i class="fas fa-coins"></i> امور مالی</a></li>
                <li class="menu-item"><a class="menu-link" onclick="showSection('parents', this)"><i class="fas fa-users"></i> ارتباط با اولیا</a></li>
                <li class="menu-item"><a class="menu-link" onclick="showSection('calendar', this)"><i class="fas fa-calendar-alt"></i> تقویم اجرایی</a></li>
            </ul>
            
            <div style="margin-top: 30px; padding: 15px; background: #e3f2fd; border-radius: 10px; text-align: center;">
                <i class="fas fa-headset" style="font-size: 30px; color: var(--primary); margin-bottom: 10px;"></i>
                <p style="font-size: 0.9rem; color: #555;">نیاز به راهنمایی دارید؟</p>
                <a href="#" style="color: var(--secondary); font-weight: bold; text-decoration: none;">تماس با مشاور</a>
            </div>
        </aside>

        <!-- Main Content -->
        <main class="content-area">
            
            <!-- SECTION: HOME -->
            <div id="home" class="section active">
                <div class="glass-card">
                    <h2 style="color:var(--primary); margin-bottom:10px;">👋 به مدرسه مهدوی خوش آمدید</h2>
                    <p>این سامانه مرجع کامل تمامی قوانین، مقررات و آیین‌نامه‌های داخلی دبیرستان دوره اول متوسطه (پایه‌های هفتم، هشتم و نهم) می‌باشد. لطفاً جهت آگاهی کامل، بخش‌های مختلف را مطالعه فرمایید.</p>
                </div>

                <div class="stats-grid">
                    <div class="stat-card">
                        <span class="stat-number">۳۲</span>
                        <span class="stat-label">ماده قانونی مصوب</span>
                    </div>
                    <div class="stat-card">
                        <span class="stat-number">۱۰۰٪</span>
                        <span class="stat-label">شفافیت آموزشی</span>
                    </div>
                    <div class="stat-card">
                        <span class="stat-number">۲۴/۷</span>
                        <span class="stat-label">دسترسی آنلاین</span>
                    </div>
                </div>

                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-bullhorn"></i> پیام مدیریت</div>
                    </div>
                    <p>دانش‌آموز عزیز، قانون در مدرسه مهدوی برای محدودیت نیست، بلکه برای ایجاد فضایی امن و عادلانه است تا استعدادهای تو شکوفا شود. رعایت این قوانین نشانه بلوغ فکری و شخصیت بالای توست.</p>
                </div>
            </div>

            <!-- SECTION: APPEARANCE -->
            <div id="appearance" class="section">
                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-user-tie"></i> آیین‌نامه پوشش و آراستگی (ویژه پسران)</div>
                    </div>
                    
                    <div class="accordion">
                        <!-- Item 1 -->
                        <div class="acc-item">
                            <div class="acc-header" onclick="toggleAcc(this)">
                                <span>۱. لباس فرم رسمی (روزهای عادی)</span>
                                <i class="fas fa-chevron-down acc-icon"></i>
                            </div>
                            <div class="acc-body">
                                <div class="acc-content">
                                    <ul>
                                        <li><strong>پیراهن:</strong> سفید یا آبی روشن (طبق مصوبه)، اتوکشیده، دکمه‌ها بسته، آستین بلند.</li>
                                        <li><strong>شلوار:</strong> پارچه‌ای سرمه‌ای یا مشکی، راسته (نه تنگ و نه بگی)، بدون زاپ و پارگی.</li>
                                        <li><strong>کمربند:</strong> چرم ساده مشکی یا قهوه‌ای الزامی است.</li>
                                        <li><strong>کفش:</strong> رسمی مشکی یا قهوه‌ای تیره. استفاده از کتانی رنگی ممنوع است.</li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                        <!-- Item 2 -->
                        <div class="acc-item">
                            <div class="acc-header" onclick="toggleAcc(this)">
                                <span>۲. وضعیت مو و صورت</span>
                                <i class="fas fa-chevron-down acc-icon"></i>
                            </div>
                            <div class="acc-body">
                                <div class="acc-content">
                                    <div class="alert-box alert-danger">
                                        <i class="fas fa-exclamation-triangle"></i>
                                        <div>موهای بلند، مدل‌های فانتزی، ساییدن دور گوش (Fade شدید) و رنگ کردن مو اکیداً ممنوع است.</div>
                                    </div>
                                    <ul>
                                        <li>موها باید کاملاً کوتاه و متعارف باشند (حداکثر ۳ سانت).</li>
                                        <li>صورت باید هر روز اصلاح شود (بدون ریش و ته‌ریش).</li>
                                        <li>استفاده از ژل و مواد حالت‌دهنده به مقدار زیاد ممنوع است.</li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                        <!-- Item 3 -->
                        <div class="acc-item">
                            <div class="acc-header" onclick="toggleAcc(this)">
                                <span>۳. ممنوعیت‌های ظاهری</span>
                                <i class="fas fa-chevron-down acc-icon"></i>
                            </div>
                            <div class="acc-body">
                                <div class="acc-content">
                                    <ul>
                                        <li>❌ هرگونه زیورآلات (گردنبند، دستبند، انگشتر تزئینی، گوشواره).</li>
                                        <li>❌ خالکوبی (تاتو) دائمی یا موقت.</li>
                                        <li>❌ لاک ناخن یا برداشتن ابرو.</li>
                                        <li>❌ استفاده از عینک دودی در داخل مدرسه.</li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- SECTION: TIME -->
            <div id="time" class="section">
                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-stopwatch"></i> قوانین حضور و غیاب و تأخیر</div>
                    </div>
                    <div class="table-container">
                        <table>
                            <thead>
                                <tr>
                                    <th>عنوان</th>
                                    <th>قانون</th>
                                    <th>جریمه / پیامد</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td>ساعت ورود</td>
                                    <td>۷:۱۵ صبح (درب ۷:۳۰ بسته می‌شود)</td>
                                    <td>-</td>
                                </tr>
                                <tr>
                                    <td>تأخیر مجاز</td>
                                    <td>ماهیانه حداکثر ۱۰ دقیقه جمعاً</td>
                                    <td>-</td>
                                </tr>
                                <tr>
                                    <td>تأخیر غیرموجه</td>
                                    <td>ورود بعد از ۷:۳۰ بدون دلیل</td>
                                    <td>ثبت در پرونده + کسر نمره انضباط</td>
                                </tr>
                                <tr>
                                    <td>غیبت موجه</td>
                                    <td>بیماری (گواهی پزشک) یا فوت بستگان</td>
                                    <td>نیاز به جبران درس</td>
                                </tr>
                                <tr>
                                    <td>غیبت غیرموجه</td>
                                    <td>هرگونه غیبت بدون اطلاع قبلی</td>
                                    <td>صفر نمره روز + احضار ولی</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                    <br>
                    <div class="alert-box alert-info">
                        <i class="fas fa-info-circle"></i>
                        <div>خروج زودهنگام از مدرسه فقط با مراجعه حضوری والدین و امضای برگه خروج امکان‌پذیر است.</div>
                    </div>
                </div>
            </div>

            <!-- SECTION: CLASSROOM -->
            <div id="classroom" class="section">
                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-school"></i> قوانین داخل کلاس درس</div>
                    </div>
                    <div class="accordion">
                        <div class="acc-item">
                            <div class="acc-header" onclick="toggleAcc(this)">
                                <span>بایدها (وظایف دانش‌آموز)</span>
                                <i class="fas fa-chevron-down acc-icon"></i>
                            </div>
                            <div class="acc-body">
                                <div class="acc-content">
                                    <ul>
                                        <li>✅ همراه داشتن کتاب و وسایل لازم در هر جلسه.</li>
                                        <li>✅ انجام تکالیف شبانه و تحویل به موقع.</li>
                                        <li>✅ سکوت و توجه هنگام تدریس معلم.</li>
                                        <li>✅ اجازه گرفتن برای صحبت یا خروج از کلاس.</li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                        <div class="acc-item">
                            <div class="acc-header" onclick="toggleAcc(this)">
                                <span>نبایدها (خط قرمزها)</span>
                                <i class="fas fa-chevron-down acc-icon"></i>
                            </div>
                            <div class="acc-body">
                                <div class="acc-content">
                                    <ul>
                                        <li>❌ خوردن و آشامیدن در کلاس (مگر آب).</li>
                                        <li>❌ شوخی‌های فیزیکی و پرتاب اشیاء.</li>
                                        <li>❌ بی‌احترامی به معلم یا تمسخر همکلاسی‌ها.</li>
                                        <li>❌ خوابیدن در کلاس درس.</li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- SECTION: EXAM -->
            <div id="exam" class="section">
                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-pen-fancy"></i> نظام ارزشیابی و امتحانات</div>
                    </div>
                    <p>نمره نهایی هر درس از ترکیب نمرات مستمر و پایانی محاسبه می‌شود:</p>
                    <div style="background: white; padding: 20px; border-radius: 10px; margin: 15px 0; border: 1px solid #eee;">
                        <div style="display:flex; justify-content:space-between; margin-bottom:10px;">
                            <span>نمرات مستمر (کلاسی):</span>
                            <span class="badge bg-blue">۲۰ نمره</span>
                        </div>
                        <div style="display:flex; justify-content:space-between; margin-bottom:10px;">
                            <span>امتحان میان‌ترم:</span>
                            <span class="badge bg-blue">۲۰ نمره</span>
                        </div>
                        <div style="display:flex; justify-content:space-between;">
                            <span>امتحان پایان‌ترم (کتبی):</span>
                            <span class="badge bg-blue">۲۰ نمره</span>
                        </div>
                    </div>
                    
                    <div class="alert-box alert-danger">
                        <i class="fas fa-ban"></i>
                        <div>
                            <strong>تقلب در امتحانات:</strong> هرگونه نگاه به برگه دیگران، استفاده از تقلب‌نامه یا تلفن همراه منجر به <strong>نمره صفر</strong> و درج در پرونده انضباطی می‌شود.
                        </div>
                    </div>
                </div>
            </div>

            <!-- SECTION: TECH -->
            <div id="tech" class="section">
                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-wifi"></i> قوانین فناوری و فضای مجازی</div>
                    </div>
                    <div class="accordion">
                        <div class="acc-item">
                            <div class="acc-header" onclick="toggleAcc(this)">
                                <span>📱 تلفن همراه و گجت‌ها</span>
                                <i class="fas fa-chevron-down acc-icon"></i>
                            </div>
                            <div class="acc-body">
                                <div class="acc-content">
                                    <p>همراه داشتن تلفن همراه (هوشمند یا ساده)، ساعت هوشمند و هندزفری در محیط مدرسه <strong>اکیداً ممنوع</strong> است.</p>
                                    <ul>
                                        <li>در صورت مشاهده، دستگاه ضبط و تنها با مراجعه والدین تحویل داده می‌شود.</li>
                                        <li>تکرار تخلف منجر به اخراج موقت می‌گردد.</li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                        <div class="acc-item">
                            <div class="acc-header" onclick="toggleAcc(this)">
                                <span>💻 اینترنت و شبکه‌های اجتماعی</span>
                                <i class="fas fa-chevron-down acc-icon"></i>
                            </div>
                            <div class="acc-body">
                                <div class="acc-content">
                                    <ul>
                                        <li>استفاده از اینترنت مدرسه فقط برای اهداف پژوهشی مجاز است.</li>
                                        <li>هرگونه قلدری سایبری، انتشار عکس خصوصی همکلاسی‌ها یا توهین در فضای مجازی پیگرد قانونی دارد.</li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

             <!-- SECTION: FACILITIES -->
             <div id="facilities" class="section">
                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-microscope"></i> اماکن تخصصی (آزمایشگاه و کارگاه)</div>
                    </div>
                    <ul>
                        <li>ورود به آزمایشگاه فقط با روپوش سفید و تحت نظارت مربی مجاز است.</li>
                        <li>شوخی با مواد شیمیایی، ابزارآلات کارگاه و تجهیزات کامپیوتری ممنوع است.</li>
                        <li>جبران خسارت وارد شده به اموال مدرسه بر عهده ولی دانش‌آموز است.</li>
                        <li>رعایت نکات ایمنی (پوشیدن عینک ایمنی در آزمایشگاه) الزامی است.</li>
                    </ul>
                </div>
            </div>

            <!-- SECTION: CAMP -->
            <div id="camp" class="section">
                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-campground"></i> مقررات اردوها</div>
                    </div>
                    <p>شرکت در اردوها نیازمند رضایت‌نامه کتبی ولی و تسویه حساب مالی است.</p>
                    <div class="alert-box alert-info">
                        <i class="fas fa-shield-alt"></i>
                        <div>در اردوها جداسازی از گروه، همراه داشتن وسایل خطرناک و خروج خودسرانه از کمپ ممنوع بوده و منجر به محرومیت دائم از اردو می‌شود.</div>
                    </div>
                </div>
            </div>

            <!-- SECTION: FINANCE -->
            <div id="finance" class="section">
                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-money-bill-wave"></i> شهریه و امور مالی</div>
                    </div>
                    <ul>
                        <li>پرداخت شهریه طبق اقساط تعیین شده در قرارداد الزامی است.</li>
                        <li>تاخیر بیش از ۱۰ روز در پرداخت اقساط منجر به توقف خدمات آموزشی (عدم صدور کارنامه) می‌شود.</li>
                        <li>هزینه کتاب‌های کمک‌درسی، لباس فرم و اردوها جدا از شهریه ثابت است.</li>
                    </ul>
                </div>
            </div>

            <!-- SECTION: PARENTS -->
            <div id="parents" class="section">
                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-handshake"></i> تعامل با اولیا</div>
                    </div>
                    <p>اولیای گرامی می‌توانند از طریق راه‌های زیر با مدرسه در ارتباط باشند:</p>
                    <div style="display: flex; gap: 15px; flex-wrap: wrap; margin-top: 15px;">
                        <div class="badge bg-blue" style="padding: 10px 20px;">📞 تلفن دفتر: ۰۲۱-XXXXXXXX</div>
                        <div class="badge bg-green" style="padding: 10px 20px;">🌐 سامانه شاد</div>
                        <div class="badge bg-blue" style="padding: 10px 20px;">📅 جلسات ماهانه دیدار با معلم</div>
                    </div>
                </div>
            </div>

            <!-- SECTION: CALENDAR -->
            <div id="calendar" class="section">
                <div class="glass-card">
                    <div class="card-header">
                        <div class="card-title"><i class="fas fa-calendar-check"></i> تقویم اجرایی سال تحصیلی</div>
                    </div>
                    <div class="timeline" style="border-right: 3px solid var(--secondary); padding-right: 20px;">
                        <div style="margin-bottom: 20px;">
                            <h4 style="color:var(--primary);">🍂 مهر ماه</h4>
                            <p>ثبت‌نام، توزیع کتب، آزمون‌های تشخیصی، شروع کلاس‌ها.</p>
                        </div>
                        <div style="margin-bottom: 20px;">
                            <h4 style="color:var(--primary);">❄️ دی ماه</h4>
                            <p>برگزاری امتحانات نوبت اول، ثبت نمرات در سامانه سیدا.</p>
                        </div>
                        <div style="margin-bottom: 20px;">
                            <h4 style="color:var(--primary);">🌱 خرداد ماه</h4>
                            <p>امتحانات پایانی نوبت دوم، جشن فارغ‌التحصیلی پایه نهم.</p>
                        </div>
                        <div>
                            <h4 style="color:var(--primary);">☀️ شهریور ماه</h4>
                            <p>امتحانات تجدیدی، ثبت‌نام سال جدید.</p>
                        </div>
                    </div>
                </div>
            </div>

        </main>
    </div>

    <script>
        // Toggle Sidebar on Mobile
        function toggleSidebar() {
            document.getElementById('sidebar').classList.toggle('show');
        }

        // Switch Sections
        function showSection(sectionId, element) {
            // Hide all sections
            document.querySelectorAll('.section').forEach(sec => sec.classList.remove('active'));
            // Show target section
            document.getElementById(sectionId).classList.add('active');
            
            // Update Menu Active State
            document.querySelectorAll('.menu-link').forEach(link => link.classList.remove('active'));
            if(element) element.classList.add('active');

            // Close sidebar on mobile after click
            if(window.innerWidth <= 992) {
                document.getElementById('sidebar').classList.remove('show');
            }
            
            // Scroll to top of content
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Accordion Logic
        function toggleAcc(header) {
            const item = header.parentElement;
            const body = header.nextElementSibling;
            
            // Toggle current
            item.classList.toggle('open');
            if (item.classList.contains('open')) {
                body.style.maxHeight = body.scrollHeight + "px";
            } else {
                body.style.maxHeight = null;
            }
        }
    </script>
</body>
</html>
