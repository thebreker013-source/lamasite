<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>لمى | موقع شخصي</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: 'Segoe UI', Tahoma, sans-serif; background: #f5f5f0; color: #2c2c2a; }

  nav { background: white; border-bottom: 1px solid #e0e0d8; display: flex; justify-content: center; gap: 8px; padding: 12px; position: sticky; top: 0; z-index: 100; }
  nav button { padding: 8px 20px; border: 1px solid #d0d0c8; border-radius: 20px; background: none; cursor: pointer; font-size: 14px; color: #555; transition: all 0.2s; }
  nav button.active, nav button:hover { background: #7F77DD; color: white; border-color: #7F77DD; }

  .hero { background: linear-gradient(135deg, #EEEDFE, #E1F5EE); text-align: center; padding: 60px 20px 40px; }
  .avatar { width: 100px; height: 100px; border-radius: 50%; background: linear-gradient(135deg, #7F77DD, #1D9E75); display: flex; align-items: center; justify-content: center; font-size: 36px; color: white; font-weight: bold; margin: 0 auto 16px; border: 4px solid white; box-shadow: 0 4px 20px rgba(127,119,221,0.3); }
  .hero h1 { font-size: 32px; color: #3C3489; }
  .hero p { color: #555; margin-top: 8px; font-size: 15px; }
  .badges { display: flex; gap: 10px; justify-content: center; margin-top: 16px; flex-wrap: wrap; }
  .badge { padding: 5px 14px; border-radius: 20px; font-size: 13px; }
  .badge.purple { background: #EEEDFE; color: #3C3489; border: 1px solid #AFA9EC; }
  .badge.teal { background: #E1F5EE; color: #085041; border: 1px solid #5DCAA5; }
  .badge.coral { background: #FAECE7; color: #712B13; border: 1px solid #F0997B; }

  .container { max-width: 750px; margin: 0 auto; padding: 30px 20px; }
  .section { display: none; }
  .section.active { display: block; }

  .card { background: white; border: 1px solid #e0e0d8; border-radius: 12px; padding: 20px; margin-bottom: 16px; }
  .card h3 { font-size: 16px; color: #3C3489; margin-bottom: 10px; }
  .card p { font-size: 14px; line-height: 1.8; color: #444; }

  .info-row { display: flex; gap: 12px; padding: 10px 0; border-bottom: 1px solid #f0f0e8; font-size: 14px; }
  .info-row:last-child { border-bottom: none; }
  .info-label { color: #888; min-width: 100px; }
  .info-val { font-weight: 600; color: #2c2c2a; }

  .skill-wrap { margin-bottom: 14px; }
  .skill-label { display: flex; justify-content: space-between; font-size: 13px; color: #666; margin-bottom: 6px; }
  .skill-bar { height: 8px; background: #f0f0e8; border-radius: 4px; overflow: hidden; }
  .skill-fill { height: 100%; border-radius: 4px; transition: width 1s ease; }
  .purple { background: #7F77DD; }
  .teal   { background: #1D9E75; }
  .coral  { background: #D85A30; }

  .projects { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 14px; }
  .proj-card { background: white; border: 1px solid #e0e0d8; border-radius: 12px; padding: 16px; }
  .proj-card .icon { font-size: 28px; margin-bottom: 10px; }
  .proj-card h4 { font-size: 14px; font-weight: 600; color: #2c2c2a; margin-bottom: 6px; }
  .proj-card p { font-size: 13px; color: #777; line-height: 1.6; }

  .contact-link { display: flex; align-items: center; gap: 12px; padding: 14px; border: 1px solid #e0e0d8; border-radius: 10px; background: white; margin-bottom: 10px; text-decoration: none; color: #2c2c2a; transition: border-color 0.2s; cursor: pointer; }
  .contact-link:hover { border-color: #7F77DD; }
  .contact-link .icon { font-size: 20px; width: 32px; text-align: center; }
  .contact-link span { font-size: 14px; }

  footer { text-align: center; padding: 30px; color: #aaa; font-size: 13px; }
</style>
</head>
<body>

<div class="hero">
  <div class="avatar">ل</div>
  <h1>لمى</h1>
  <p>مصممة UI/UX · مطورة Front-end · مبدعة رقمية</p>
  <div class="badges">
    <span class="badge purple">🎨 تصميم</span>
    <span class="badge teal">💻 برمجة</span>
    <span class="badge coral">✨ إبداع</span>
  </div>
</div>

<nav>
  <button class="active" onclick="show('about', this)">عني</button>
  <button onclick="show('skills', this)">مهاراتي</button>
  <button onclick="show('projects', this)">أعمالي</button>
  <button onclick="show('contact', this)">تواصل</button>
</nav>

<div class="container">

  <div id="about" class="section active">
    <div class="card">
      <h3>من أنا؟</h3>
      <p>مرحباً! أنا لمى، مصممة ومطورة شغوفة بإنشاء تجارب رقمية جميلة وسهلة الاستخدام. أجمع بين الإبداع والتقنية لأبني منتجات تُحدث فرقاً حقيقياً.</p>
    </div>
    <div class="card">
      <div class="info-row"><span class="info-label">الاسم</span><span class="info-val">لمى</span></div>
      <div class="info-row"><span class="info-label">التخصص</span><span class="info-val">تصميم وتطوير واجهات</span></div>
      <div class="info-row"><span class="info-label">الموقع</span><span class="info-val">السعودية 🇸🇦</span></div>
      <div class="info-row"><span class="info-label">الخبرة</span><span class="info-val">+5 سنوات</span></div>
      <div class="info-row"><span class="info-label">اللغات</span><span class="info-val">العربية · الإنجليزية</span></div>
    </div>
  </div>

  <div id="skills" class="section">
    <div class="card">
      <h3>المهارات التقنية</h3>
      <div class="skill-wrap">
        <div class="skill-label"><span>UI/UX Design</span><span>95%</span></div>
        <div class="skill-bar"><div class="skill-fill purple" style="width:95%"></div></div>
      </div>
      <div class="skill-wrap">
        <div class="skill-label"><span>Figma</span><span>90%</span></div>
        <div class="skill-bar"><div class="skill-fill purple" style="width:90%"></div></div>
      </div>
      <div class="skill-wrap">
        <div class="skill-label"><span>React / Next.js</span><span>85%</span></div>
        <div class="skill-bar"><div class="skill-fill teal" style="width:85%"></div></div>
      </div>
      <div class="skill-wrap">
        <div class="skill-label"><span>CSS / Tailwind</span><span>88%</span></div>
        <div class="skill-bar"><div class="skill-fill coral" style="width:88%"></div></div>
      </div>
      <div class="skill-wrap">
        <div class="skill-label"><span>JavaScript</span><span>80%</span></div>
        <div class="skill-bar"><div class="skill-fill teal" style="width:80%"></div></div>
      </div>
    </div>
  </div>

  <div id="projects" class="section">
    <div class="projects">
      <div class="proj-card">
        <div class="icon">🎨</div>
        <h4>نظام تصميم موحد</h4>
        <p>بناء Design System كامل لشركة ناشئة من الصفر</p>
      </div>
      <div class="proj-card">
        <div class="icon">📱</div>
        <h4>تطبيق Lama Shop</h4>
        <p>تطبيق تسوق بواجهة أنيقة وتجربة مستخدم سلسة</p>
      </div>
      <div class="proj-card">
        <div class="icon">📊</div>
        <h4>لوحة تحليلات</h4>
        <p>Dashboard تفاعلي لعرض البيانات بشكل مرئي</p>
      </div>
      <div class="proj-card">
        <div class="icon">🎓</div>
        <h4>منصة تعليمية</h4>
        <p>تصميم وتطوير منصة إلكترونية للتعلم عن بُعد</p>
      </div>
    </div>
  </div>

  <div id="contact" class="section">
    <div class="card">
      <h3>تواصل معي</h3>
      <div class="contact-link"><span class="icon">📧</span><span>lama@example.com</span></div>
      <div class="contact-link"><span class="icon">📸</span><span>@lama.designs</span></div>
      <div class="contact-link"><span class="icon">💼</span><span>lama-designer</span></div>
      <div class="contact-link"><span class="icon">💻</span><span>lama-dev</span></div>
    </div>
  </div>

</div>

<footer>لمى · 2026</footer>

<script>
function show(id, btn) {
  document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
  document.querySelectorAll('nav button').forEach(b => b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  btn.classList.add('active');
}
</script>
</body>
</html>
