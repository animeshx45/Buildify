<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>DukaanSite</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">

<style>

/* =========================
   GLOBAL STYLES
========================= */

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

html{
  scroll-behavior:smooth;
}

body{
  font-family:'Poppins',sans-serif;
  background:#ffffff;
  color:#111827;
  overflow-x:hidden;
  line-height:1.8;
}

/* =========================
   HERO SECTION
========================= */

.hero{
  position:relative;
  overflow:hidden;
  padding:100px 25px;
  border-radius:0 0 40px 40px;
  background:linear-gradient(135deg,#020617,#0f172a,#1e293b);
  color:white;
  text-align:center;
  animation:fadeIn 1.2s ease;
}

.glow1,
.glow2{
  position:absolute;
  border-radius:50%;
  filter:blur(130px);
  opacity:0.18;
}

.glow1{
  width:350px;
  height:350px;
  background:#38bdf8;
  top:-100px;
  left:-100px;
  animation:pulse 6s infinite alternate;
}

.glow2{
  width:320px;
  height:320px;
  background:#8b5cf6;
  bottom:-120px;
  right:-120px;
  animation:pulse 5s infinite alternate;
}

.hero img{
  width:110px;
  animation:float 4s ease-in-out infinite;
  position:relative;
  z-index:2;
}

.hero h1{
  font-size:6em;
  margin-top:20px;
  font-weight:900;
  background:linear-gradient(90deg,#38bdf8,#818cf8,#22c55e);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  line-height:1.1;
  position:relative;
  z-index:2;
}

.hero p{
  max-width:850px;
  margin:auto;
  margin-top:25px;
  font-size:1.4em;
  color:#cbd5e1;
  position:relative;
  z-index:2;
}

.hero .btn{
  display:inline-block;
  margin-top:35px;
  background:linear-gradient(90deg,#38bdf8,#6366f1);
  color:white;
  text-decoration:none;
  padding:18px 42px;
  border-radius:50px;
  font-size:1.15em;
  font-weight:700;
  transition:0.4s;
  box-shadow:0 10px 30px rgba(56,189,248,0.35);
  position:relative;
  z-index:2;
}

.hero .btn:hover{
  transform:scale(1.08);
}

/* =========================
   MARQUEE
========================= */

.marquee-container{
  width:100%;
  overflow:hidden;
  background:linear-gradient(90deg,#0f172a,#111827,#1e293b);
  padding:18px 0;
}

.marquee{
  display:flex;
  width:max-content;
  animation:scrollText 26s linear infinite;
}

.marquee span{
  color:white;
  font-size:1.3em;
  font-weight:700;
  margin-right:60px;
  white-space:nowrap;
  transition:0.3s;
}

.marquee span:hover{
  color:#38bdf8;
  transform:scale(1.08);
}

/* =========================
   SECTIONS
========================= */

.section{
  padding:90px 8%;
}

.section-title{
  text-align:center;
  font-size:3.6em;
  margin-bottom:50px;
  font-weight:800;
  color:#0f172a;
}

.section-content{
  background:linear-gradient(145deg,#ffffff,#f8fafc);
  padding:45px;
  border-radius:28px;
  box-shadow:0 10px 30px rgba(0,0,0,0.08);
  font-size:1.18em;
  color:#334155;
}

/* =========================
   CARDS
========================= */

.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
  gap:25px;
}

.card{
  background:linear-gradient(145deg,#0f172a,#1e293b);
  color:white;
  padding:35px;
  border-radius:24px;
  transition:0.4s;
  box-shadow:0 10px 25px rgba(0,0,0,0.18);
}

.card:hover{
  transform:translateY(-10px);
  box-shadow:0 18px 35px rgba(56,189,248,0.22);
}

.card h3{
  font-size:1.9em;
  margin-bottom:15px;
}

.card p{
  font-size:1.12em;
  color:#cbd5e1;
}

/* =========================
   GLASS CARDS
========================= */

.glass-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:25px;
}

.glass-card{
  background:rgba(255,255,255,0.75);
  backdrop-filter:blur(12px);
  border:1px solid rgba(255,255,255,0.5);
  padding:35px;
  border-radius:24px;
  transition:0.4s;
  box-shadow:0 10px 25px rgba(0,0,0,0.06);
}

.glass-card:hover{
  transform:translateY(-10px);
}

.glass-card h3{
  font-size:1.8em;
  margin-bottom:14px;
}

.glass-card p{
  font-size:1.08em;
  color:#475569;
}

/* =========================
   FUTURE SECTION
========================= */

.future{
  background:linear-gradient(135deg,#020617,#111827);
  color:white;
  border-radius:28px;
  padding:50px;
  box-shadow:0 15px 40px rgba(0,0,0,0.35);
}

.future ul{
  list-style:none;
}

.future li{
  margin:20px 0;
  font-size:1.2em;
}

/* =========================
   VISION
========================= */

.vision{
  background:#f8fafc;
  border-left:6px solid #38bdf8;
  padding:45px;
  border-radius:24px;
  font-size:1.18em;
  color:#334155;
  box-shadow:0 10px 25px rgba(0,0,0,0.08);
}

/* =========================
   CTA
========================= */

.cta{
  margin:90px 8%;
  padding:70px 25px;
  border-radius:30px;
  text-align:center;
  background:linear-gradient(135deg,#38bdf8,#6366f1);
  color:white;
  box-shadow:0 15px 40px rgba(99,102,241,0.35);
}

.cta h2{
  font-size:3.5em;
}

.cta p{
  max-width:750px;
  margin:auto;
  margin-top:20px;
  font-size:1.2em;
  color:#e2e8f0;
}

.cta a{
  display:inline-block;
  margin-top:35px;
  background:white;
  color:#111827;
  text-decoration:none;
  padding:18px 40px;
  border-radius:50px;
  font-size:1.15em;
  font-weight:700;
  transition:0.4s;
}

.cta a:hover{
  transform:scale(1.08);
}

/* =========================
   FOOTER
========================= */

footer{
  text-align:center;
  padding:40px 20px;
  color:#64748b;
  font-size:1.05em;
}

/* =========================
   ANIMATIONS
========================= */

@keyframes scrollText{
  0%{
    transform:translateX(100%);
  }
  100%{
    transform:translateX(-100%);
  }
}

@keyframes float{
  0%{
    transform:translateY(0px);
  }
  50%{
    transform:translateY(-12px);
  }
  100%{
    transform:translateY(0px);
  }
}

@keyframes pulse{
  from{
    transform:scale(1);
  }
  to{
    transform:scale(1.2);
  }
}

@keyframes fadeIn{
  from{
    opacity:0;
    transform:translateY(40px);
  }
  to{
    opacity:1;
    transform:translateY(0);
  }
}

/* =========================
   MOBILE RESPONSIVE
========================= */

@media(max-width:768px){

  .hero h1{
    font-size:3.8em;
  }

  .section-title{
    font-size:2.5em;
  }

  .cta h2{
    font-size:2.4em;
  }

  .hero p,
  .section-content,
  .vision,
  .future li{
    font-size:1.02em;
  }

  .marquee span{
    font-size:1em;
  }

}

</style>
</head>

<body>

<!-- HERO -->

<section class="hero">

<div class="glow1"></div>
<div class="glow2"></div>

<img src="https://img.icons8.com/fluency/120/shop.png">

<h1>DukaanSite</h1>

<p>
✨ AI-Powered No-Code Website Builder for Modern Businesses
</p>

<p>
Build stunning, fast, and professional websites in minutes —
without writing a single line of code.
</p>

<a href="#" class="btn">🚀 Launch Your Website</a>

</section>

<!-- RUNNING TEXT -->

<div class="marquee-container">

<div class="marquee">

<span>🚀 AI Website Builder</span>
<span>✨ No Coding Needed</span>
<span>⚡ Lightning Fast Websites</span>
<span>📱 Mobile Responsive</span>
<span>🔍 SEO Optimized</span>
<span>🛒 E-Commerce Ready</span>
<span>🌍 Empowering Local Businesses</span>
<span>💼 Professional Modern UI</span>
<span>🔒 Secure & Reliable</span>
<span>🚀 DukaanSite 2026</span>

</div>

</div>

<!-- ABOUT -->

<section class="section">

<h2 class="section-title">🌟 What is DukaanSite?</h2>

<div class="section-content">

DukaanSite helps local shops, restaurants, startups, creators, and businesses build premium websites instantly using AI.

<br><br>

No coding. No expensive developers. No complicated setup.

<br><br>

Everything from design, content, responsiveness, SEO, and performance is automatically handled to create a modern professional website experience.

<br><br>

✨ Think of it as your own digital agency powered by AI.

</div>

</section>

<!-- FEATURES -->

<section class="section">

<h2 class="section-title">⚡ Powerful Features</h2>

<div class="grid">

<div class="card">
<h3>🤖 AI Website Generation</h3>
<p>Automatically creates layouts, colors, content, and sections intelligently.</p>
</div>

<div class="card">
<h3>⚡ Ultra Fast Speed</h3>
<p>Optimized performance for faster loading and better customer experience.</p>
</div>

<div class="card">
<h3>📱 Mobile Responsive</h3>
<p>Looks perfect across phones, tablets, desktops, and laptops.</p>
</div>

<div class="card">
<h3>🔍 SEO Optimized</h3>
<p>Improves visibility on Google and helps businesses grow online.</p>
</div>

<div class="card">
<h3>🔒 Advanced Security</h3>
<p>Enterprise-grade protection with reliable secure infrastructure.</p>
</div>

<div class="card">
<h3>🌍 Multi-language Support</h3>
<p>Create websites in English, Hindi, and regional languages.</p>
</div>

</div>

</section>

<!-- WEBSITE TYPES -->

<section class="section">

<h2 class="section-title">🎨 Website Categories</h2>

<div class="glass-grid">

<div class="glass-card">
<h3>🛒 E-Commerce</h3>
<p>Shopping carts, checkout systems, and online stores.</p>
</div>

<div class="glass-card">
<h3>🍽️ Restaurants</h3>
<p>Menus, table booking systems, and elegant food layouts.</p>
</div>

<div class="glass-card">
<h3>👗 Fashion Brands</h3>
<p>Premium modern showcase websites for fashion businesses.</p>
</div>

<div class="glass-card">
<h3>🎓 Education</h3>
<p>Course portals and coaching institute websites.</p>
</div>

<div class="glass-card">
<h3>🎭 Portfolios</h3>
<p>Beautiful portfolio websites for creators and freelancers.</p>
</div>

<div class="glass-card">
<h3>💼 Corporate</h3>
<p>Professional business websites and admin dashboards.</p>
</div>

</div>

</section>

<!-- FUTURE -->

<section class="section">

<h2 class="section-title">🚀 Why DukaanSite is Future Ready</h2>

<div class="future">

<ul>

<li>✨ AI continuously improves automation and website quality.</li>

<li>📈 Scalable infrastructure for thousands of businesses.</li>

<li>🌍 Built with modern global web standards.</li>

<li>📱 Adapts to future devices and changing trends.</li>

<li>⚡ Speed and SEO optimized by default.</li>

</ul>

</div>

</section>

<!-- VISION -->

<section class="section">

<h2 class="section-title">🌍 Our Vision</h2>

<div class="vision">

We believe every local business deserves a premium online presence.

<br><br>

Whether it's a bakery, tuition center, restaurant, boutique, or startup —
DukaanSite empowers businesses with world-class digital experiences without needing technical knowledge.

<br><br>

✨ Our mission is simple:
<b>Transform local shops into trusted online brands.</b>

</div>

</section>

<!-- CTA -->

<section class="cta">

<h2>🚀 Ready to Build Your Website?</h2>

<p>
Create modern, fast, and professional websites powered by AI —
without coding or technical complexity.
</p>

<a href="#">✨ Get Started Today</a>

</section>

<!-- FOOTER -->

<footer>

✨ From Local Shop to Global Brand ✨

<br><br>

Made with ❤️ for modern businesses · DukaanSite © 2026

</footer>

</body>
</html>
