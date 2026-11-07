<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#0b1020">
<title>SATWIK | Website Testing Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500;600;700&family=DM+Sans:wght@400;600&display=swap" rel="stylesheet">
<style>
:root{--bg:#0b1020;--surface:#131a33;--ink:#e8ecff;--muted:#9aa4cc;--line:#252e54;--a:#7c8cff;--b:#3ee0c4;--grad:linear-gradient(135deg,#7c8cff,#3ee0c4);box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:light){:root:not([data-theme="dark"]){--bg:#f5f7ff;--surface:#fff;--ink:#141a38;--muted:#555f88;--line:#d9def2;--a:#4457e6;--b:#0b8f79;--grad:linear-gradient(135deg,#4457e6,#0b8f79)}}
:root[data-theme="light"]{--bg:#f5f7ff;--surface:#fff;--ink:#141a38;--muted:#555f88;--line:#d9def2;--a:#4457e6;--b:#0b8f79;--grad:linear-gradient(135deg,#4457e6,#0b8f79)}
html{scroll-behavior:smooth;scroll-padding-top:4.5rem}
*,*::before,*::after{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font:400 1.0625rem/1.65 "DM Sans",system-ui,sans-serif}
h1,h2,h3{font-family:Poppins,system-ui,sans-serif;line-height:1.15;margin:0}
a{color:inherit}
a:focus-visible{outline:3px solid var(--b);outline-offset:3px}
p{margin:.7rem 0;max-width:62ch}
nav{position:sticky;top:env(safe-area-inset-top,0px);z-index:5;background:var(--bg);border-bottom:1px solid var(--line)}
.wrap{max-width:60rem;margin:0 auto;padding:0 1.25rem}
nav .wrap{display:flex;flex-wrap:wrap;gap:.4rem 1.4rem;align-items:center;justify-content:space-between;padding-top:.8rem;padding-bottom:.8rem}
.logo{font:700 1.15rem Poppins,sans-serif;text-decoration:none}
.logo span{color:var(--b)}
nav ul{display:flex;flex-wrap:wrap;gap:.2rem 1.1rem;list-style:none;margin:0;padding:0;font-size:.95rem}
nav ul a{text-decoration:none;color:var(--muted)}
nav ul a:hover{color:var(--ink)}
nav ul a{display:inline-block;padding:.25rem 0}
@media(max-width:560px){
  nav .wrap{display:grid;justify-content:start;gap:.45rem}
  nav ul{gap:.15rem 1rem;font-size:.88rem}
  section{padding-top:2.6rem}
}
section{padding:3.5rem 0 1rem}
.kicker{color:var(--b);font-weight:600;margin:0}
h1{font-size:clamp(2.1rem,8vw,3.4rem);font-weight:700;letter-spacing:-.02em;margin-top:.5rem}
h2{font-size:clamp(1.6rem,5vw,2.1rem);font-weight:700;margin-top:.3rem}
h3{font-size:1.15rem;font-weight:600}
.hero{position:relative;isolation:isolate;display:grid;gap:2rem;align-items:center}
@media (min-width:760px){.hero{grid-template-columns:1.3fr 1fr}}
.btns{display:flex;flex-wrap:wrap;gap:.7rem;margin-top:1.4rem}
.btn{display:inline-block;padding:.7rem 1.3rem;border-radius:99px;font-weight:600;text-decoration:none;border:1px solid var(--line)}
.btn.main{background:var(--grad);color:#0b1020;border-color:transparent}
.btn:hover{filter:brightness(1.1)}
.card{background:var(--surface);border:1px solid var(--line);border-radius:14px;padding:1.3rem}
.hero .card h3{margin:.6rem 0 .2rem}
.icons{font-size:1.6rem;letter-spacing:.4rem}
.chips{display:flex;flex-wrap:wrap;gap:.5rem;list-style:none;padding:0;margin:1rem 0 0}
.chips li{border:1px solid var(--line);background:var(--surface);padding:.25rem .85rem;border-radius:99px;font-size:.95rem}
.grid{display:grid;gap:1rem;margin-top:1.4rem}
@media (min-width:760px){.grid{grid-template-columns:repeat(3,1fr)}}
.tag{color:var(--a);font-weight:600;font-size:.85rem;margin:.6rem 0 .2rem}
.card ul{padding-left:1.1rem;margin:.6rem 0 0;color:var(--muted)}
.emoji{font-size:1.8rem}
.scroll{overflow-x:auto;margin-top:1.4rem;border:1px solid var(--line);border-radius:14px}
table{border-collapse:collapse;width:100%;min-width:36rem;background:var(--surface)}
th,td{text-align:left;padding:.8rem 1rem;border-bottom:1px solid var(--line);vertical-align:top}
th{color:var(--muted);font-weight:600;font-size:.92rem}
tr:last-child td{border-bottom:0}
.tip{color:var(--muted);font-size:.97rem}
footer{margin-top:3.5rem;padding:1.4rem 0 2.5rem;border-top:1px solid var(--line);color:var(--muted);font-size:.92rem}
@keyframes rise{from{opacity:0;transform:translateY(22px)}to{opacity:1;transform:none}}
@keyframes float{50%{transform:translateY(-8px)}}
@keyframes shine{to{background-position:200% center}}
@media (prefers-reduced-motion:no-preference){
.hero>div:first-child>*{animation:rise .7s ease-out both}
.hero>div:first-child>:nth-child(2){animation-delay:.1s}
.hero>div:first-child>:nth-child(3){animation-delay:.2s}
.hero>div:first-child>:nth-child(4){animation-delay:.3s}
.hero .card{animation:rise .8s .35s ease-out both}
.icons{display:inline-block;animation:float 3s ease-in-out infinite}
.logo span{display:inline-block;animation:float 2s ease-in-out infinite}
.btn.main{background-size:200% auto;animation:shine 4s linear infinite}
.js .reveal{opacity:0;transform:translateY(24px);transition:opacity .6s ease-out,transform .6s ease-out}
.js .reveal.in{opacity:1;transform:none}
.grid>.card:nth-child(2){transition-delay:.12s}
.grid>.card:nth-child(3){transition-delay:.24s}
.btn{transition:transform .2s,filter .2s}
.btn:hover{transform:translateY(-2px)}
.chips li{transition:transform .2s,border-color .2s}
.chips li:hover{transform:translateY(-3px);border-color:var(--a)}
tbody tr{transition:background .2s}
tbody tr:hover{background:var(--line)}
}
main{overflow-x:clip}
.orb{position:absolute;z-index:-1;border-radius:50%;filter:blur(60px);opacity:.35;pointer-events:none}
.o1{width:18rem;height:18rem;background:var(--a);top:-4rem;left:-5rem}
.o2{width:16rem;height:16rem;background:var(--b);bottom:-4rem;right:-3rem}
.progress{position:fixed;left:0;right:0;top:env(safe-area-inset-top,0px);height:3px;background:var(--grad);transform:scaleX(0);transform-origin:left;z-index:10}
.type{font:600 1.1rem Poppins,sans-serif;color:var(--b);min-height:1.7em;margin:.9rem 0 0}
.caret{display:inline-block;width:2px;height:1.1em;background:currentColor;margin-left:3px;vertical-align:-.15em}
@keyframes drift{50%{transform:translate(30px,-24px) scale(1.12)}}
@keyframes blink{50%{opacity:0}}
@media (prefers-reduced-motion:no-preference){
.o1{animation:drift 9s ease-in-out infinite}
.o2{animation:drift 11s ease-in-out infinite reverse}
.caret{animation:blink 1s steps(1) infinite}
.hero>div:first-child>:nth-child(5){animation-delay:.4s}
}
.card{position:relative}
.card::before{content:"";position:absolute;inset:0;border:1px solid transparent;border-radius:14px;background:linear-gradient(135deg,var(--a),var(--b)) border-box;mask:linear-gradient(#000 0 0) padding-box,linear-gradient(#000 0 0);mask-composite:exclude;pointer-events:none;opacity:.32}
.logo{color:var(--ink)}
.logo span{color:var(--b)}
.progress{background:var(--grad)}
.btn.main{background:var(--grad);background-size:100% 100%}
@media (prefers-reduced-motion:no-preference){
  .card::before{transition:opacity .2s ease}
  .card:hover::before{opacity:.75}
}
@media (prefers-reduced-motion:reduce){.progress{display:none}}
@media (prefers-reduced-motion:reduce){html{scroll-behavior:auto}}
</style>
</head>
<body>
<div class="progress" aria-hidden="true"></div>
<nav><div class="wrap">
<a class="logo" href="#home">SATWIK<span>.</span></a>
<ul><li><a href="#about">About</a></li><li><a href="#projects">Practice Projects</a></li><li><a href="#reports">Sample Bug Reports</a></li><li><a href="#contact">Contact</a></li></ul>
</div></nav>

<main class="wrap">
<section id="home" class="hero">
<div>
<p class="kicker">Beginner · Manual Website Testing</p>
<h1>Hi, I’m SATWIK. I test websites with care.</h1>
<p>I’m learning manual website testing and building my skills through practice test cases, login checks, shopping-cart scenarios, and clear sample bug reports.</p>
<p class="type" aria-label="I check login flows, shopping carts, forms and mobile layouts">I check <span id="word">login flows</span><span class="caret" aria-hidden="true"></span></p>
<div class="btns"><a class="btn main" href="#projects">Explore practice work ↓</a><a class="btn" href="#contact">Contact details</a></div>
</div>
<div class="card">
<div class="icons" aria-hidden="true">⌘ ✓</div>
<h3>Quality starts with curiosity.</h3>
<p style="color:var(--muted);margin:.2rem 0">Careful steps. Clear evidence. Helpful reports.</p>
<ul class="chips"><li>Manual QA</li><li>Test Cases</li><li>Bug Reports</li></ul>
</div>
<div class="orb o1" aria-hidden="true"></div><div class="orb o2" aria-hidden="true"></div>
</section>

<section id="about">
<p class="kicker">About me</p>
<h2>Learning to find issues before users do.</h2>
<p>I’m a beginner website tester focused on understanding expected versus actual behavior, writing clear reproduction steps, and documenting findings in a structured way. The examples on this page are practice samples, not claims of paid client work.</p>
<ul class="chips"><li>Manual Testing Basics</li><li>Login Test Scenarios</li><li>Shopping Cart Scenarios</li><li>Expected vs Actual Results</li><li>Severity &amp; Priority Basics</li><li>Test Case Writing</li></ul>
</section>

<section id="projects">
<p class="kicker">Selected learning work</p>
<h2>Practice projects</h2>
<p>Sample scenarios created for learning. These are not verified findings from a live client website.</p>
<div class="grid">
<article class="card"><div class="emoji" aria-hidden="true">🔐</div><p class="tag">PRACTICE PROJECT</p><h3>Login Testing</h3><p>Practice checking common sign-in scenarios and expected responses.</p><ul><li>Valid credentials should allow sign-in.</li><li>Incorrect password should show a clear error.</li><li>Empty required fields should be validated.</li></ul></article>
<article class="card"><div class="emoji" aria-hidden="true">🛒</div><p class="tag">PRACTICE PROJECT</p><h3>Shopping Cart Testing</h3><p>Practice verifying cart updates and totals.</p><ul><li>Add a product and verify it appears.</li><li>Remove a product and verify it disappears.</li><li>Change quantity and check the displayed total.</li></ul></article>
<article class="card"><div class="emoji" aria-hidden="true">🧪</div><p class="tag">PRACTICE PROJECT</p><h3>Test Cases &amp; Bug Reports</h3><p>Practice writing reproducible, easy-to-understand QA notes.</p><ul><li>Write preconditions and steps.</li><li>Record expected and actual results.</li><li>Suggest severity and priority for review.</li></ul></article>
</div>
</section>

<section id="reports">
<p class="kicker">Example documentation</p>
<h2>Sample bug reports</h2>
<p>These are hypothetical training examples to demonstrate reporting format. They have not been confirmed on a real product.</p>
<div class="scroll"><table>
<thead><tr><th>Sample title</th><th>Expected result</th><th>Hypothetical actual result</th><th>Suggested severity</th></tr></thead>
<tbody>
<tr><td>Login remains on sign-in page</td><td>Valid test credentials should open the home page.</td><td>For this sample scenario, the page remains on sign-in.</td><td>High (example only)</td></tr>
<tr><td>Removed cart item still appears</td><td>Removed product should no longer appear in the cart.</td><td>For this sample scenario, the item remains visible.</td><td>Medium (example only)</td></tr>
<tr><td>Cart total does not update</td><td>Total should reflect the selected quantity and price.</td><td>For this sample scenario, the total stays unchanged.</td><td>Medium (example only)</td></tr>
</tbody></table></div>
<p class="tip">Tip: In a real report, include the test environment, clear reproduction steps, relevant screenshots, and the observed result. Only report a bug after reproducing it.</p>
</section>

<section id="contact">
<p class="kicker">Contact</p>
<h2>Let’s connect</h2>
<p>I’m open to learning opportunities and beginner-friendly website testing work.</p>
<div class="card" style="margin-top:1.2rem;max-width:30rem">
<h3>Contact me</h3>
<p style="margin-bottom:1rem"><strong>Email:</strong> <a href="mailto:satwikpottapogula058@gmail.com">satwikpottapogula058@gmail.com</a></p>
<a class="btn main" href="mailto:satwikpottapogula058@gmail.com">Send an email</a>
</div>
</section>

<footer>© 2026 SATWIK · Beginner Website Testing Portfolio · Sample work is for practice only.</footer>
</main>
<script>
(function(){
  var root=document.documentElement;
  try{
    if(!("IntersectionObserver" in window)||window.matchMedia("(prefers-reduced-motion:reduce)").matches)return;
    var els=document.querySelectorAll("section:not(#home) > :not(.grid), .grid > .card");
    var io=new IntersectionObserver(function(entries){
      entries.forEach(function(entry){
        if(entry.isIntersecting){entry.target.classList.add("in");io.unobserve(entry.target)}
      });
    },{threshold:.12});
    els.forEach(function(el){el.classList.add("reveal");io.observe(el)});
    root.classList.add("js");
  }catch(error){
    root.classList.remove("js");
    document.querySelectorAll(".reveal").forEach(function(el){el.classList.remove("reveal","in")});
  }
})();
</script>
<script>
(function(){try{
if(matchMedia("(prefers-reduced-motion:reduce)").matches)return;
var bar=document.querySelector(".progress"),t=false;
if(!bar)return;
function upd(){var h=document.documentElement.scrollHeight-window.innerHeight;bar.style.transform="scaleX("+(h>0?Math.min(window.scrollY/h,1):0)+")";t=false}
function scheduleUpdate(){if(!t){t=true;requestAnimationFrame(upd)}}
addEventListener("scroll",scheduleUpdate,{passive:true});
addEventListener("resize",scheduleUpdate,{passive:true});
addEventListener("orientationchange",scheduleUpdate,{passive:true});
upd();
var w=document.getElementById("word"),words=["login flows","shopping carts","forms","mobile layouts"],i=0,n=0,del=false;
function tick(){var s=words[i];n+=del?-1:1;w.textContent=s.slice(0,n);var d=del?40:80;
if(!del&&n===s.length){del=true;d=1300}else if(del&&n===0){del=false;i=(i+1)%words.length;d=300}
setTimeout(tick,d)}
w.textContent="";setTimeout(tick,900);
}catch(x){}})();
</script>
</body>
</html>
