<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>مدرسة الصداقة التشادية السودانية</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;500;600;700;800;900&display=swap');

:root{
  --dark:#003d30;
  --dark2:#004b3b;
  --green:#07543f;
  --green2:#0b674d;
  --light:#176b54;
  --gold:#f7cc45;
  --gold2:#ffd966;
  --white:#ffffff;
  --soft:#eaf7f1;
  --glass:rgba(255,255,255,.09);
  --border:rgba(255,255,255,.22);
  --shadow:0 15px 40px rgba(0,0,0,.22);
}

*{
  box-sizing:border-box;
  margin:0;
  padding:0;
  scroll-behavior:smooth;
}

body{
  font-family:'Cairo',sans-serif;
  background:
    radial-gradient(circle at 15% 20%,rgba(247,204,69,.12),transparent 28%),
    radial-gradient(circle at 90% 70%,rgba(0,255,180,.08),transparent 30%),
    linear-gradient(135deg,#003d30,#07543f 45%,#06432f);
  color:white;
  line-height:1.9;
}

a{
  color:inherit;
  text-decoration:none;
}

.container{
  width:92%;
  max-width:1150px;
  margin:auto;
}

/* الشريط العلوي */
.top-bar{
  height:7px;
  background:linear-gradient(
    90deg,
    #111 0 20%,
    #d21f26 20% 38%,
    #f7cc45 38% 55%,
    #0b6b4f 55% 78%,
    #0865a5 78% 100%
  );
}

/* الهيدر */
header{
  background:rgba(0,45,35,.96);
  border-bottom:1px solid rgba(255,255,255,.08);
  position:sticky;
  top:0;
  z-index:999;
  backdrop-filter:blur(15px);
}

.nav{
  min-height:105px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
}

.logo{
  display:flex;
  align-items:center;
  gap:15px;
}

.logo-icon{
  width:68px;
  height:68px;
  border-radius:22px;
  background:linear-gradient(145deg,#ffd95b,#f0b936);
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:39px;
  box-shadow:0 8px 25px rgba(247,204,69,.22);
}

.logo-text h2{
  color:var(--gold);
  font-size:20px;
  line-height:1.4;
}

.logo-text p{
  font-size:12px;
  color:#d8e8e2;
}

nav{
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
  gap:8px;
}

nav a{
  padding:10px 12px;
  border-radius:12px;
  color:#eef8f4;
  font-size:14px;
  transition:.3s;
}

nav a:hover{
  background:rgba(247,204,69,.14);
  color:var(--gold);
}

/* الهيرو */
.hero{
  min-height:650px;
  display:flex;
  align-items:center;
  position:relative;
  overflow:hidden;
  background:
    radial-gradient(circle at 15% 60%,rgba(247,204,69,.16),transparent 25%),
    radial-gradient(circle at 85% 20%,rgba(0,180,130,.18),transparent 30%),
    linear-gradient(135deg,#064b37,#075d45 50%,#003d30);
}

.hero::before{
  content:"";
  position:absolute;
  width:420px;
  height:420px;
  border:1px solid rgba(255,255,255,.07);
  border-radius:50%;
  right:-180px;
  top:-100px;
}

.hero-content{
  position:relative;
  z-index:2;
  text-align:center;
  width:100%;
}

.flags{
  font-size:52px;
  letter-spacing:8px;
  margin-bottom:18px;
}

.badge{
  display:inline-block;
  padding:8px 22px;
  border:1px solid rgba(255,255,255,.25);
  border-radius:40px;
  background:rgba(255,255,255,.07);
  color:#ffe28a;
  font-size:16px;
  margin-bottom:22px;
  backdrop-filter:blur(10px);
}

.hero h1{
  font-size:clamp(38px,7vw,75px);
  font-weight:900;
  line-height:1.3;
  margin-bottom:20px;
}

.hero h1 span{
  color:var(--gold);
}

.hero p{
  max-width:800px;
  margin:0 auto 30px;
  color:#e1eee9;
  font-size:19px;
}

.buttons{
  display:flex;
  justify-content:center;
  flex-wrap:wrap;
  gap:15px;
}

.btn{
  padding:15px 28px;
  border-radius:40px;
  border:1px solid rgba(255,255,255,.35);
  font-size:17px;
  font-weight:700;
  transition:.3s;
  display:inline-block;
}

.btn-gold{
  background:linear-gradient(135deg,#f5c83f,#ffdc63);
  color:#164a39;
  box-shadow:0 10px 25px rgba(247,204,69,.2);
}

.btn-outline{
  background:rgba(255,255,255,.06);
  color:white;
}

.btn:hover{
  transform:translateY(-4px);
}

/* الأقسام */
section{
  padding:85px 0;
}

.section-title{
  text-align:center;
  margin-bottom:45px;
}

.section-title small{
  color:var(--gold);
  font-weight:700;
  font-size:15px;
}

.section-title h2{
  font-size:38px;
  margin-top:5px;
}

.section-title p{
  color:#cde1d9;
  max-width:650px;
  margin:10px auto;
}

/* بطاقة عامة */
.card{
  background:linear-gradient(
    145deg,
    rgba(255,255,255,.105),
    rgba(255,255,255,.045)
  );
  border:1px solid var(--border);
  border-radius:28px;
  padding:30px;
  box-shadow:var(--shadow);
  backdrop-filter:blur(12px);
}

.card:hover{
  border-color:rgba(247,204,69,.4);
}

/* عن المدرسة */
.about-grid{
  display:grid;
  grid-template-columns:1.1fr .9fr;
  gap:25px;
}

.about-card h3{
  color:var(--gold);
  margin-bottom:12px;
  font-size:25px;
}

.about-card p{
  color:#d9eae4;
}

/* الإحصائيات */
.stats{
  background:rgba(0,30,23,.28);
}

.stats-grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:18px;
}

.stat{
  text-align:center;
  padding:30px 15px;
  border-radius:25px;
  background:rgba(255,255,255,.07);
  border:1px solid rgba(255,255,255,.14);
}

.stat-icon{
  font-size:32px;
}

.stat strong{
  display:block;
  color:var(--gold);
  font-size:34px;
}

.stat span{
  color:#d9e8e2;
}

/* الرؤية */
.triple{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
}

.info-card{
  text-align:center;
  padding:35px 25px;
}

.info-card .icon{
  font-size:48px;
  margin-bottom:12px;
}

.info-card h3{
  color:var(--gold);
  font-size:23px;
  margin-bottom:10px;
}

.info-card p{
  color:#d5e6df;
}

/* الصداقة */
.friendship{
  padding:55px 20px;
  text-align:center;
  background:
    linear-gradient(
      135deg,
      rgba(0,61,48,.7),
      rgba(9,101,75,.65)
    );
  border-top:1px solid rgba(255,255,255,.1);
  border-bottom:1px solid rgba(255,255,255,.1);
}

.friendship .flags{
  margin-bottom:8px;
}

.friendship h2{
  color:var(--gold);
  font-size:34px;
}

/* المواد */
.subjects{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:15px;
}

.subject{
  padding:20px;
  border-radius:20px;
  background:rgba(255,255,255,.075);
  border:1px solid rgba(255,255,255,.15);
  font-weight:700;
  text-align:center;
  transition:.3s;
}

.subject:hover{
  background:rgba(247,204,69,.12);
  border-color:rgba(247,204,69,.4);
  transform:translateY(-4px);
}

.subject span{
  display:block;
  font-size:30px;
  margin-bottom:5px;
}

/* الإدارة */
.people{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
}

.person{
  text-align:center;
}

.person .avatar{
  width:80px;
  height:80px;
  border-radius:50%;
  margin:auto auto 15px;
  display:flex;
  align-items:center;
  justify-content:center;
  background:linear-gradient(145deg,#f7cc45,#dba82e);
  color:#164a39;
  font-size:34px;
}

.person h3{
  color:white;
}

.person p{
  color:#cbded7;
}

/* الأخبار */
.news{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
}

.news-card{
  overflow:hidden;
  padding:0;
}

.news-top{
  padding:22px;
  background:rgba(247,204,69,.1);
  font-size:38px;
}

.news-body{
  padding:25px;
}

.news-body h3{
  color:var(--gold);
  margin-bottom:8px;
}

.news-body p{
  color:#d5e5df;
}

/* الأنشطة */
.activities{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:15px;
}

.activity{
  text-align:center;
  padding:28px 15px;
}

.activity-icon{
  font-size:45px;
  margin-bottom:10px;
}

.activity h3{
  color:var(--gold);
  font-size:18px;
}

/* تيك توك */
.tiktok{
  text-align:center;
}

.tiktok-box{
  max-width:700px;
  margin:auto;
  padding:45px 25px;
  background:
    linear-gradient(
      135deg,
      rgba(255,255,255,.1),
      rgba(255,255,255,.045)
    );
  border:1px solid rgba(255,255,255,.2);
  border-radius:32px;
  box-shadow:var(--shadow);
}

.tiktok-logo{
  font-size:65px;
  margin-bottom:10px;
}

.tiktok-box h2{
  color:var(--gold);
  margin-bottom:10px;
}

.tiktok-box p{
  color:#d5e6df;
  margin-bottom:25px;
}

/* الموقع */
.location{
  text-align:center;
}

.map-box{
  max-width:850px;
  margin:auto;
  padding:45px 25px;
}

.map-icon{
  font-size:65px;
}

.map-box h2{
  color:var(--gold);
  margin:10px 0;
}

.map-box p{
  color:#d8e7e1;
  margin-bottom:25px;
}

/* الفوتر */
footer{
  background:#002d23;
  padding:45px 20px 25px;
  border-top:1px solid rgba(255,255,255,.1);
  text-align:center;
}

.footer-logo{
  color:var(--gold);
  font-size:24px;
  font-weight:800;
}

footer p{
  color:#bfd5cd;
  margin:8px 0;
}

.copyright{
  margin-top:25px;
  padding-top:20px;
  border-top:1px solid rgba(255,255,255,.1);
  color:#8eafa3;
  font-size:13px;
}

/* زر الصعود */
#top{
  position:fixed;
  bottom:22px;
  left:22px;
  width:58px;
  height:58px;
  border-radius:50%;
  border:none;
  background:linear-gradient(145deg,#f7cc45,#ffd968);
  color:#164a39;
  font-size:25px;
  font-weight:bold;
  cursor:pointer;
  box-shadow:0 10px 25px rgba(0,0,0,.3);
  z-index:1000;
}

/* الهاتف */
@media(max-width:800px){

  .nav{
    padding:18px 0;
    flex-direction:column;
  }

  nav{
    width:100%;
  }

  nav a{
    font-size:13px;
    padding:7px 8px;
  }

  .hero{
    min-height:620px;
  }

  .flags{
    font-size:43px;
  }

  .hero h1{
    font-size:43px;
  }

  .hero p{
    font-size:17px;
  }

  .about-grid,
  .triple,
  .people,
  .news{
    grid-template-columns:1fr;
  }

  .stats-grid{
    grid-template-columns:repeat(2,1fr);
  }

  .subjects{
    grid-template-columns:repeat(2,1fr);
  }

  .activities{
    grid-template-columns:repeat(2,1fr);
  }

  section{
    padding:65px 0;
  }

  .section-title h2{
    font-size:31px;
  }
}

@media(max-width:480px){

  .container{
    width:90%;
  }

  .logo-text h2{
    font-size:17px;
  }

  .logo-icon{
    width:58px;
    height:58px;
    font-size:32px;
  }

  .hero h1{
    font-size:38px;
  }

  .hero p{
    font-size:16px;
  }

  .buttons{
    flex-direction:column;
    align-items:center;
  }

  .btn{
    width:90%;
  }

  .stats-grid{
    grid-template-columns:1fr 1fr;
  }

  .subjects{
    grid-template-columns:1fr 1fr;
  }

  .activities{
    grid-template-columns:1fr 1fr;
  }

  .card{
    padding:24px 18px;
  }
}
</style>
</head>

<body>

<div class="top-bar"></div>

<header>
  <div class="container nav">

    <div class="logo">
      <div class="logo-icon">🏫</div>

      <div class="logo-text">
        <h2>مدرسة الصداقة التشادية السودانية</h2>
        <p>العلم يجمعنا • الصداقة توحدنا • المستقبل هدفنا</p>
      </div>
    </div>

    <nav>
      <a href="#home">الرئيسية</a>
      <a href="#about">عن المدرسة</a>
      <a href="#vision">الرؤية</a>
      <a href="#subjects">الدراسة</a>
      <a href="#admin">الإدارة</a>
      <a href="#news">الأخبار</a>
      <a href="#activities">الأنشطة</a>
      <a href="#location">الموقع</a>
    </nav>

  </div>
</header>


<!-- الرئيسية -->
<section class="hero" id="home">
  <div class="container hero-content">

    <div class="flags">🇸🇩 🤝 🇹🇩</div>

    <div class="badge">🎓 تعليم • أخلاق • معرفة • طموح</div>

    <h1>
      مدرسة <span>الصداقة</span><br>
      التشادية <span>السودانية</span>
    </h1>

    <p>
      هنا يبدأ طريق العلم، وتُبنى الشخصية، وتنمو المواهب
      لصناعة جيل واعٍ ومتعلّم وقادر على صناعة مستقبل أفضل.
    </p>

    <div class="buttons">
      <a href="#about" class="btn btn-gold">✨ اكتشف المدرسة</a>
      <a href="#subjects" class="btn btn-outline">📚 المواد الدراسية</a>
    </div>

  </div>
</section>


<!-- عن المدرسة -->
<section id="about">
  <div class="container">

    <div class="section-title">
      <small>من نحن</small>
      <h2>عن المدرسة</h2>
      <p>بيئة تعليمية تهدف إلى بناء المعرفة والشخصية معاً.</p>
    </div>

    <div class="about-grid">

      <div class="card about-card">
        <h3>🏫 مدرستنا</h3>
        <p>
          مدرسة الصداقة التشادية السودانية مؤسسة تعليمية تهتم
          بالعلم والتربية وبناء جيل يمتلك المعرفة والقيم والمهارات
          التي تساعده على النجاح وخدمة مجتمعه.
        </p>
      </div>

      <div class="card about-card">
        <h3>🤝 رسالة الصداقة</h3>
        <p>
          نؤمن بأن التعليم جسر للتعاون والتواصل، وأن الصداقة
          بين الشعبين التشادي والسوداني قيمة جميلة تستحق أن
          تُغرس في الأجيال القادمة.
        </p>
      </div>

    </div>
  </div>
</section>


<!-- الإحصائيات -->
<section class="stats">
  <div class="container">

    <div class="section-title">
      <small>أرقامنا</small>
      <h2>مدرستنا في لمحة</h2>
    </div>

    <div class="stats-grid">

      <div class="stat">
        <div class="stat-icon">🎓</div>
        <strong>18+</strong>
        <span>مادة دراسية</span>
      </div>

      <div class="stat">
        <div class="stat-icon">📚</div>
        <strong>∞</strong>
        <span>فرص للتعلم</span>
      </div>

      <div class="stat">
        <div class="stat-icon">🌟</div>
        <strong>100%</strong>
        <span>طموح للمستقبل</span>
      </div>

      <div class="stat">
        <div class="stat-icon">🤝</div>
        <strong>2</strong>
        <span>شعب يجمعهما التعليم</span>
      </div>

    </div>
  </div>
</section>


<!-- الرؤية والرسالة والقيم -->
<section id="vision">
  <div class="container">

    <div class="section-title">
      <small>هويتنا التعليمية</small>
      <h2>رؤيتنا ورسالتنا وقيمنا</h2>
    </div>

    <div class="triple">

      <div class="card info-card">
        <div class="icon">🔭</div>
        <h3>الرؤية</h3>
        <p>
          بناء جيل متعلم، مبدع، واثق بنفسه وقادر على المساهمة
          في صناعة مستقبل أفضل.
        </p>
      </div>

      <div class="card info-card">
        <div class="icon">🎯</div>
        <h3>الرسالة</h3>
        <p>
          تقديم تعليم متوازن يجمع بين المعرفة والأخلاق
          والمهارات والتفكير والإبداع.
        </p>
      </div>

      <div class="card info-card">
        <div class="icon">💎</div>
        <h3>القيم</h3>
        <p>
          الاحترام • الأمانة • التعاون • الاجتهاد • المسؤولية
          • الانتماء • الإبداع.
        </p>
      </div>

    </div>
  </div>
</section>


<!-- الصداقة التشادية السودانية -->
<div class="friendship">
  <div class="flags">🇸🇩 🤝 🇹🇩</div>
  <h2>الصداقة التشادية السودانية</h2>
  <p>
    التعليم يجمعنا والصداقة توحدنا والمستقبل يجمع طموحنا.
  </p>
</div>


<!-- المواد -->
<section id="subjects">
  <div class="container">

    <div class="section-title">
      <small>التعليم والمعرفة</small>
      <h2>المواد الدراسية</h2>
      <p>مجموعة متنوعة من المواد لبناء معرفة متكاملة.</p>
    </div>

    <div class="subjects">

      <div class="subject"><span>📖</span>اللغة العربية</div>
      <div class="subject"><span>🇬🇧</span>اللغة الإنجليزية</div>
      <div class="subject"><span>➗</span>الرياضيات</div>
      <div class="subject"><span>🔬</span>العلوم</div>
      <div class="subject"><span>⚗️</span>الكيمياء</div>
      <div class="subject"><span>🧬</span>الأحياء</div>
      <div class="subject"><span>⚛️</span>الفيزياء</div>
      <div class="subject"><span>🌍</span>الجغرافيا</div>
      <div class="subject"><span>📜</span>التاريخ</div>
      <div class="subject"><span>💻</span>الحاسوب</div>
      <div class="subject"><span>🎨</span>التربية الفنية</div>
      <div class="subject"><span>⚽</span>التربية الرياضية</div>
      <div class="subject"><span>🕌</span>التربية الإسلامية</div>
      <div class="subject"><span>🧠</span>المهارات الحياتية</div>
      <div class="subject"><span>🌱</span>البيئة</div>
      <div class="subject"><span>💬</span>التواصل</div>
      <div class="subject"><span>💰</span>الاقتصاد</div>
      <div class="subject"><span>⚖️</span>التربية المدنية</div>

    </div>
  </div>
</section>


<!-- الإدارة -->
<section id="admin">
  <div class="container">

    <div class="section-title">
      <small>فريق المدرسة</small>
      <h2>الإدارة والمعلمون</h2>
      <p>فريق يعمل من أجل تعليم أفضل.</p>
    </div>

    <div class="people">

      <div class="card person">
        <div class="avatar">👨‍💼</div>
        <h3>إدارة المدرسة</h3>
        <p>قيادة وتنظيم العملية التعليمية</p>
      </div>

      <div class="card person">
        <div class="avatar">👨‍🏫</div>
        <h3>المعلمون</h3>
        <p>تعليم وتوجيه وتنمية المواهب</p>
      </div>

      <div class="card person">
        <div class="avatar">👩‍💼</div>
        <h3>الطاقم الإداري</h3>
        <p>دعم وتنظيم وخدمة الطلاب</p>
      </div>

    </div>
  </div>
</section>


<!-- الأخبار -->
<section id="news">
  <div class="container">

    <div class="section-title">
      <small>آخر المستجدات</small>
      <h2>أخبار المدرسة</h2>
    </div>

    <div class="news">

      <div class="card news-card">
        <div class="news-top">📢</div>
        <div class="news-body">
          <h3>إعلانات المدرسة</h3>
          <p>
            تابعوا هنا آخر الإعلانات والمعلومات المهمة الخاصة بالمدرسة.
          </p>
        </div>
      </div>

      <div class="card news-card">
        <div class="news-top">🎓</div>
        <div class="news-body">
          <h3>النجاح والتفوق</h3>
          <p>
            نحتفي بطلابنا ونشجعهم دائماً على الاجتهاد والتفوق.
          </p>
        </div>
      </div>

      <div class="card news-card">
        <div class="news-top">🌟</div>
        <div class="news-body">
          <h3>فعاليات المدرسة</h3>
          <p>
            أنشطة تعليمية وثقافية ورياضية لتنمية مهارات الطلاب.
          </p>
        </div>
      </div>

    </div>
  </div>
</section>


<!-- الأنشطة -->
<section id="activities">
  <div class="container">

    <div class="section-title">
      <small>الحياة المدرسية</small>
      <h2>الأنشطة</h2>
    </div>

    <div class="activities">

      <div class="card activity">
        <div class="activity-icon">⚽</div>
        <h3>الرياضة</h3>
      </div>

      <div class="card activity">
        <div class="activity-icon">🎨</div>
        <h3>الفنون</h3>
      </div>

      <div class="card activity">
        <div class="activity-icon">📚</div>
        <h3>القراءة</h3>
      </div>

      <div class="card activity">
        <div class="activity-icon">🧪</div>
        <h3>العلوم</h3>
      </div>

    </div>
  </div>
</section>


<!-- تيك توك -->
<section class="tiktok">
  <div class="container">

    <div class="section-title">
      <small>تابع المدرسة</small>
      <h2>حساب TikTok</h2>
    </div>

    <div class="tiktok-box">

      <div class="tiktok-logo">🎵</div>

      <h2>مدرسة الصداقة التشادية السودانية</h2>

      <p>
        تابع آخر أخبار المدرسة وأنشطتها ومقاطعها على TikTok.
      </p>

      <a
        href="https://www.tiktok.com/@dyrdm93vtpy4?_r=1&_t=ZS-9A7D7ReSiiy"
        target="_blank"
        class="btn btn-gold"
      >
        🎵 فتح حساب TikTok
      </a>

    </div>

  </div>
</section>


<!-- الموقع -->
<section id="location">
  <div class="container">

    <div class="section-title">
      <small>موقعنا</small>
      <h2>موقع المدرسة</h2>
    </div>

    <div class="card map-box">

      <div class="map-icon">📍</div>

      <h2>أبشي — تشاد</h2>

      <p>
        يمكنك الوصول إلى موقع مدرسة الصداقة التشادية السودانية
        عبر خرائط Google.
      </p>

      <a
        href="https://maps.app.goo.gl/e8hdEEoPZeVEeMdZ8?g_st=ac"
        target="_blank"
        class="btn btn-gold"
      >
        📍 فتح الموقع على Google Maps
      </a>

    </div>

  </div>
</section>


<!-- الفوتر -->
<footer>

  <div class="footer-logo">
    🇸🇩 مدرسة الصداقة التشادية السودانية 🇹🇩
  </div>

  <p>
    العلم يجمعنا • الصداقة توحدنا • المستقبل هدفنا
  </p>

  <p>
    أبشي — تشاد
  </p>

  <div class="copyright">
    © 2026 مدرسة الصداقة التشادية السودانية — جميع الحقوق محفوظة
  </div>

</footer>


<!-- زر العودة للأعلى -->
<button id="top" onclick="window.scrollTo({top:0,behavior:'smooth'})">
  ↑
</button>


</body>
</html>
