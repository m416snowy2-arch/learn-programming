<!doctype html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>دليل سنة أولى - شعبة نظم (فضائي بنفسجي)</title>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg-dark:#0b0226;
      --bg-mid:#2e0854;
      --purple-1:#7c3aed;
      --purple-2:#a78bfa;
      --glass: rgba(255,255,255,0.04);
      --muted: rgba(255,255,255,0.78);
      --card: linear-gradient(135deg, rgba(124,58,237,0.08), rgba(167,139,250,0.03));
      --radius:14px;
    }
    *{box-sizing:border-box}
    html,body{height:100%;}
    body{
      margin:0; font-family:'Cairo',sans-serif;
      background:
        radial-gradient(800px 400px at 10% 10%, rgba(167,139,250,0.04), transparent),
        linear-gradient(180deg,var(--bg-dark),var(--bg-mid));
      color:#eef2ff;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      scroll-behavior:smooth;
    }

    /* stars background */
    .stars { position:fixed; inset:0; z-index:0; pointer-events:none; }
    .star { position:absolute; border-radius:50%; background:rgba(255,255,255,0.9); opacity:0.12; animation:twinkle 6s infinite; }
    @keyframes twinkle { 0%,100%{opacity:0.08}50%{opacity:0.25} }

    header{
      position:sticky; top:0; z-index:50;
      display:flex; align-items:center; justify-content:space-between;
      padding:12px 20px; gap:16px;
      backdrop-filter: blur(6px);
      background: linear-gradient(180deg, rgba(4,2,10,0.35), rgba(4,2,10,0.15));
      border-bottom: 1px solid rgba(255,255,255,0.03);
    }
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:54px;height:54px;border-radius:12px;background:linear-gradient(135deg,var(--purple-1),var(--purple-2));display:flex;align-items:center;justify-content:center;font-weight:800;color:#041025;box-shadow:0 8px 30px rgba(124,58,237,0.18)}
    .brand h1{font-size:18px;margin:0}
    nav{display:flex;gap:12px;align-items:center}
    nav a{color:var(--muted);text-decoration:none;padding:8px 10px;border-radius:8px;font-weight:600;transition:all .22s}
    nav a:hover{background:rgba(255,255,255,0.03); color:#fff; transform:translateY(-3px)}
    .menu-toggle{display:none}

    /* hero */
    .hero{max-width:1200px;margin:28px auto 14px;padding:26px;display:grid;grid-template-columns:1fr 420px;gap:22px;z-index:10;position:relative}
    .card{background:var(--card);padding:22px;border-radius:16px;box-shadow:0 18px 40px rgba(2,6,23,0.6);border:1px solid rgba(255,255,255,0.03)}
    .hero-title{font-size:28px;margin:0 0 8px}
    .hero-sub{color:var(--muted);margin-bottom:12px}
    .actions{display:flex;gap:10px}
    .btn{padding:10px 14px;border-radius:10px;border:none;cursor:pointer;font-weight:700}
    .btn.primary{background:linear-gradient(90deg,var(--purple-1),var(--purple-2));color:#061024}
    .btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.05);color:var(--muted)}

    /* illustration */
    .illu{display:flex;flex-direction:column;align-items:center;gap:12px}
    .planet{width:100%;height:300px;border-radius:12px;background:radial-gradient(circle at 20% 25%, rgba(255,255,255,0.04), transparent), linear-gradient(135deg,#6d28d9,#a78bfa);display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden}
    .planet svg{width:240px;opacity:0.98;filter:drop-shadow(0 10px 30px rgba(124,58,237,0.18))}

    main{max-width:1100px;margin:12px auto;padding:0 20px 80px;position:relative;z-index:10}
    section.card{margin-bottom:18px;opacity:0;transform:translateY(18px);transition:all .7s cubic-bezier(.2,.9,.2,1)}
    section.card.visible{opacity:1;transform:none}
    section h2{margin:0 0 10px;color:var(--purple-2);font-size:22px}
    .two-col{display:grid;grid-template-columns:1fr 360px;gap:18px;align-items:start}
    .topic{display:flex;gap:12px;align-items:flex-start}
    .icon{width:64px;height:64px;border-radius:12px;background:rgba(255,255,255,0.03);display:flex;align-items:center;justify-content:center;font-size:28px}
    .muted{color:var(--muted);font-size:14px}
    pre{background:rgba(0,0,0,0.25);padding:12px;border-radius:10px;overflow:auto;color:#e9f3ff}
    .copy-btn{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:6px 8px;border-radius:8px;color:var(--muted);cursor:pointer;font-weight:700;margin-left:8px}
    table.kws{width:100%;border-collapse:collapse;margin-top:12px}
    table.kws th, table.kws td{padding:10px;border-bottom:1px dashed rgba(255,255,255,0.03);text-align:right}
    table.kws th{color:var(--purple-2);font-weight:800}

    /* exercises */
    .exercise{background:rgba(255,255,255,0.02);padding:12px;border-radius:10px;margin-top:12px}
    .exercise button{margin-top:8px}

    footer{max-width:1100px;margin:20px auto 80px;padding:16px;text-align:center;color:var(--muted)}

    /* responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr; padding:20px}
      nav{display:none}
      .menu-toggle{display:block;background:transparent;border:1px solid rgba(255,255,255,0.06);padding:8px 10px;border-radius:8px;color:var(--muted)}
      .two-col{grid-template-columns:1fr}
      .planet{height:200px}
    }
  </style>
</head>
<body>

  <!-- decorative stars -->
  <div class="stars" aria-hidden="true">
    <!-- small JS will inject some stars -->
  </div>

  <header>
    <div class="brand">
      <div class="logo">ن</div>
      <div>
        <h1>منهج سنة أولى — شعبة نظم</h1>
        <div style="font-size:12px;color:var(--muted)">دليل تفاعلي بنفسجي فضائي — مرتب خطوة بخطوة</div>
      </div>
    </div>

    <nav id="mainNav" aria-label="navigation">
      <a href="#home">الرئيسية</a>
      <a href="#csintro">مقدمة الحاسب</a>
      <a href="#prog">البرمجة</a>
      <a href="#math">رياضيات</a>
      <a href="#stats">إحصاء</a>
      <a href="#eng">انجليزي</a>
      <a href="#mis">نظم المعلومات</a>
      <a class="cta" href="#extras">المصادر</a>
    </nav>

    <button class="menu-toggle" id="menuBtn">قائمة ☰</button>
  </header>

  <!-- HERO -->
  <section class="hero" id="home">
    <div class="card">
      <h2 class="hero-title">مرحباً يا يوسف — خريطة سنة أولى نظم (مكبرة ومنظمة)</h2>
      <p class="hero-sub">شرح مكثف، خطوات عملية بالترتيب، أمثلة قابلة للتجربة، وجداول مصطلحات. كل قسم يحتوي على خطوات تنفيذية لتبدأ وتتطور.</p>
      <div class="actions">
        <button class="btn primary" onclick="scrollToId('prog')">ابدأ من البرمجة</button>
        <button class="btn ghost" onclick="scrollToId('csintro')">مقدمة الحاسب</button>
      </div>
      <p style="margin-top:12px;color:var(--muted);font-size:13px">مهم: أنسخ الأكواد ثم جربها على Python أو Console لـJS. في كل مثال زر نسخ لتسهيل التجربة.</p>
    </div>

    <div class="illu card">
      <div class="planet" aria-hidden="true">
        <!-- astronaut SVG -->
        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="rocket">
          <defs>
            <linearGradient id="g1" x1="0" x2="1">
              <stop offset="0" stop-color="#fff" stop-opacity="0.12"/>
              <stop offset="1" stop-color="#fff" stop-opacity="0.04"/>
            </linearGradient>
          </defs>
          <g transform="translate(0,0)">
            <circle cx="100" cy="100" r="80" fill="url(#g1)"/>
            <g transform="translate(40,32)">
              <path d="M50 2 C70 2 90 20 90 42 C90 64 70 82 50 82 C30 82 10 64 10 42 C10 20 30 2 50 2 Z" fill="#fff" opacity="0.08"/>
              <path d="M50 8 C66 8 80 22 80 38 C80 54 66 68 50 68 C34 68 20 54 20 38 C20 22 34 8 50 8 Z" fill="#fff" opacity="0.12"/>
            </g>
          </g>
        </svg>
      </div>
      <div style="text-align:center;color:var(--muted)">تصميم فضائي، تحريك ناعم، وتجربة تفاعلية ✨</div>
    </div>
  </section>

  <main>

    <!-- CS Intro -->
    <section class="card" id="csintro">
      <h2>مقدمة في الحاسب</h2>
      <div class="two-col">
        <div>
          <div class="topic">
            <div class="icon">💻</div>
            <div>
              <p class="muted">ما الذي ستدرسه: مكونات الحاسب (CPU, RAM, Storage)، نظام التشغيل، وبيئة التطوير.</p>
              <ol class="muted">
                <li><b>الخطوة 1:</b> افتح الجهاز وتعرف على مكونات الهاردوير (CPU, RAM, HDD/SSD).</li>
                <li><b>الخطوة 2:</b> ثبّت نظام تشغيل حديث (Windows/Linux) وجرب فتح Task Manager/Terminal.</li>
                <li><b>الخطوة 3:</b> نزّل محرر كود VS Code وتعلم كيفية فتح Terminal داخله.</li>
              </ol>
            </div>
          </div>

          <div class="exercise">
            <strong>تمرين عملي:</strong>
            <p class="muted">نزّل Python من python.org وثبت VS Code. افتح Terminal واكتب: <code>python --version</code></p>
          </div>
        </div>

        <aside>
          <div class="card" style="padding:12px;background:rgba(255,255,255,0.02)">
            <h4 style="margin:0 0 8px">ملاحظة للبدء</h4>
            <p class="muted">لو عندك موبايل، يمكنك تجربة الأكواد الأساسية على تطبيقات مثل Pydroid أو Termux.</p>
          </div>
        </aside>
      </div>
    </section>

    <!-- Programming -->
    <section class="card" id="prog">
      <h2>أساسيات البرمجة — شرح + خطوات عملية</h2>
      <p class="muted">الجزء الأهم: متغيرات، أنواع بيانات، شروط، حلقات، ودوال. هنا خطوات لتتعلم عملياً.</p>

      <div style="display:grid;grid-template-columns:1fr 360px;gap:14px;margin-top:14px">
        <div>
          <div class="topic">
            <div class="icon">🔢</div>
            <div>
              <h3 style="margin:0;color:#fff">المتغيرات وأنواع البيانات</h3>
              <p class="muted">تعريف متغير: اسم يخزن قيمة. أمثلة عملية بلغة Python وJavaScript.</p>
              <pre id="py1"># Python example
name = "يوسف"
age = 20
print(f"مرحباً {name}, عمرك {age}")</pre>
              <button class="copy-btn" data-target="py1">نسخ الكود</button>
            </div>
          </div>

          <div class="topic" style="margin-top:12px">
            <div class="icon">🔁</div>
            <div>
              <h3 style="margin:0;color:#fff">الحلقات (Loops)</h3>
              <p class="muted">مثال JS لطباعة الأرقام 1..5</p>
              <pre id="js1">// JavaScript example
for (let i = 1; i <= 5; i++) {
  console.log(i);
}</pre>
              <button class="copy-btn" data-target="js1">نسخ الكود</button>
            </div>
          </div>
        </div>

        <aside>
          <div style="background:rgba(255,255,255,0.02);padding:12px;border-radius:10px">
            <h4 style="margin:0 0 8px">دليل تعليمي سريع (خطوات)</h4>
            <ol class="muted">
              <li><b>تنصيب:</b> قم بتثبيت Python وNode.js إذا أردت تجربة JS محلياً.</li>
              <li><b>تشغيل مثال Python:</b> افتح Terminal واكتب <code>python script.py</code>.</li>
              <li><b>تشغيل مثال JS:</b> افتح DevTools Console في المتصفح للصق وتشغيل كود JS.</li>
            </ol>
          </div>
        </aside>
      </div>

      <hr style="border:none;border-top:1px dashed rgba(255,255,255,0.04);margin:14px 0">

      <div>
        <h4 style="margin:0 0 8px">تمرين — اعمل دالة لإيجاد أكبر رقم في قائمة</h4>
        <div class="exercise muted">
          <p>الخطوات:</p>
          <ol>
            <li>اكتب دالة تأخذ مصفوفة أعداد.</li>
            <li>استعمل حلقة أو دالة جاهزة لإيجاد أكبر قيمة.</li>
            <li>اطبع النتيجة وجربها.</li>
          </ol>
          <pre id="py2"># حل بسيط في Python
def max_in_list(arr):
    maxv = arr[0]
    for x in arr:
        if x > maxv:
            maxv = x
    return maxv

print(max_in_list([3,5,1,9,2]))  # => 9</pre>
          <button class="copy-btn" data-target="py2">نسخ الحل</button>
        </div>
      </div>

      <table class="kws" aria-label="keywords">
        <tr><th>EN</th><th>AR</th><th>مثال</th></tr>
        <tr><td>Variable</td><td>متغير</td><td><code>let x = 5;</code></td></tr>
        <tr><td>Function</td><td>دالة</td><td><code>def f():</code></td></tr>
        <tr><td>Loop</td><td>حلقة</td><td><code>for (...) {}</code></td></tr>
        <tr><td>Array/List</td><td>مصفوفة/قائمة</td><td><code>[1,2,3]</code></td></tr>
      </table>
    </section>

    <!-- Math -->
    <section class="card" id="math">
      <h2>رياضيات الحاسب — خطوات للسنة الأولي</h2>
      <div class="two-col">
        <div>
          <p class="muted">مصفوفات، متجهات، وحساب مشتقات أساسية. خطوات للتدريب:</p>
          <ol class="muted">
            <li>ابدأ بفهم مصفوفة 2x2 وكيفية جمعها وضربها يدوياً.</li>
            <li>اكتب دالة Python تضرب مصفوفتين 2x2.</li>
            <li>تعلم قواعد التفاضل (مثل مشتقة x^n = n*x^(n-1)).</li>
          </ol>
          <div class="exercise">
            <strong>مثال برمجي:</strong>
            <pre id="pyMat"># ضرب مصفوفتين 2x2 في Python
def mul2x2(A,B):
    return [
      [A[0][0]*B[0][0] + A[0][1]*B[1][0], A[0][0]*B[0][1] + A[0][1]*B[1][1]],
      [A[1][0]*B[0][0] + A[1][1]*B[1][0], A[1][0]*B[0][1] + A[1][1]*B[1][1]]
    ]

print(mul2x2([[1,2],[3,4]], [[5,6],[7,8]]))</pre>
            <button class="copy-btn" data-target="pyMat">نسخ الكود</button>
          </div>
        </div>
        <aside>
          <div style="background:rgba(255,255,255,0.02);padding:12px;border-radius:10px">
            <h4 style="margin:0 0 8px">نصيحة مذاكرة</h4>
            <p class="muted">حل مسائل كثير باليد ثم اطبقها برمجياً — هذا يجعل الفهم أعمق.</p>
          </div>
        </aside>
      </div>
    </section>

    <!-- Stats -->
    <section class="card" id="stats">
      <h2>إحصاء واحتمالات</h2>
      <p class="muted">تعلم الوسط، الوسيط، التباين، والانحراف المعياري — خطوات وأمثلة.</p>
      <div class="exercise">
        <strong>تمرين عملى:</strong>
        <p class="muted">احسب الوسط والانحراف لمجموعة أرقام باستخدام Python (مثال بالأسفل).</p>
        <pre id="pyStats">import statistics
data = [10,12,23,23,16,23,21,16]
print("Mean:", statistics.mean(data))
print("StdDev:", statistics.pstdev(data))</pre>
        <button class="copy-btn" data-target="pyStats">نسخ الكود</button>
      </div>
    </section>

    <!-- English -->
    <section class="card" id="eng">
      <h2>اللغة الإنجليزية الأكاديمية</h2>
      <p class="muted">كيفية كتابة مقدمة مشروع، قراءة مراجع، ومصطلحات تقنية مهمة.</p>
      <div class="topic">
        <div class="icon">📝</div>
        <div>
          <h3 style="margin:0;color:#fff">نموذج مقدمة مشروع</h3>
          <pre id="engIntro">This project demonstrates a basic web application that teaches programming fundamentals. It includes examples and exercises for beginners.</pre>
          <button class="copy-btn" data-target="engIntro">نسخ</button>
        </div>
      </div>
    </section>

    <!-- MIS -->
    <section class="card" id="mis">
      <h2>مقدمة نظم المعلومات (MIS)</h2>
      <p class="muted">ERD, نمذجة البيانات، قواعد بيانات وعمليات CRUD.</p>
      <div class="exercise">
        <strong>تمرين:</strong>
        <p class="muted">صمم جدول طلاب (id, name, grade) وكتابة SQL لإضافة سجل جديد.</p>
        <pre id="sql1">INSERT INTO students (id, name, grade) VALUES (1, 'علي', 82);</pre>
        <button class="copy-btn" data-target="sql1">نسخ SQL</button>
      </div>
    </section>

    <!-- extras -->
    <section class="card" id="extras">
      <h2>المصادر والتمارين</h2>
      <p class="muted">قوائم تمارين منظمة لتطبيق ما تعلمته في كل مادة.</p>
      <ol class="muted">
        <li>مشروع بسيط: موقع شخصي يعرض معلوماتك (HTML/CSS).</li>
        <li>مشروع: برنامج لحساب درجات الطلاب واحتساب المتوسط (Python).</li>
        <li>قواعد بيانات: نموذج CRUD صغير لإدارة الكتب.</li>
      </ol>
      <div class="exercise">
        <button class="btn primary" onclick="alert('ابدأ بمشروع صغير: صفحة HTML تحتوي على اسمك وصورتك. ارسل لي لو حابب أراجع')">اقترح مشروع للبدء</button>
      </div>
    </section>

  </main>

  <footer>
    مصمم خصيصاً ليك يا يوسف — مرجع سنة أولى نظم (بنفسجي فضائي). © 2025
  </footer>

  <script>
    // 1) Generate stars decor
    (function makeStars(){
      const container = document.querySelector('.stars');
      const count = 45;
      for(let i=0;i<count;i++){
        const s = document.createElement('div');
        s.className='star';
        const size = Math.random()*3 + 1;
        s.style.width = s.style.height = size + 'px';
        s.style.left = Math.random()*100 + '%';
        s.style.top = Math.random()*100 + '%';
        s.style.opacity = 0.06 + Math.random()*0.2;
        s.style.animationDelay = (Math.random()*6)+'s';
        container.appendChild(s);
      }
    })();

    // 2) IntersectionObserver reveal
    const sections = document.querySelectorAll('section.card');
    const io = new IntersectionObserver(entries=>{
      entries.forEach(en=>{
        if(en.isIntersecting) en.target.classList.add('visible');
      });
    }, {threshold:0.12});
    sections.forEach(s => io.observe(s));

    // 3) Copy buttons for code examples
    document.querySelectorAll('.copy-btn').forEach(btn=>{
      btn.addEventListener('click', ()=>{
        const id = btn.getAttribute('data-target');
        const el = document.getElementById(id);
        if(!el) return;
        navigator.clipboard.writeText(el.innerText).then(()=>{
          btn.textContent='✓ تم النسخ';
          setTimeout(()=>btn.textContent='نسخ الكود',1200);
        }).catch(()=>{ alert('فشل النسخ — انسخ يدوياً')});
      });
      // set initial text
      btn.textContent = 'نسخ الكود';
    });

    // 4) Mobile menu toggle
    const menuBtn = document.getElementById('menuBtn');
    const nav = document.getElementById('mainNav');
    menuBtn.addEventListener('click', ()=>{
      if(nav.style.display === 'flex'){ nav.style.display = 'none'; }
      else { nav.style.display = 'flex'; nav.style.flexDirection='column'; nav.style.position='absolute'; nav.style.top='64px'; nav.style.right='18px'; nav.style.background='rgba(4,2,10,0.6)'; nav.style.borderRadius='10px'; nav.style.padding='10px'; }
    });

    // 5) helper to scroll
    function scrollToId(id){ document.getElementById(id).scrollIntoView({behavior:'smooth', block:'start'}); }
    window.scrollToId = scrollToId;
  </script>
</body>
</html>
