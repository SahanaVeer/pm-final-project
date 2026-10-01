[final-presentation.html](https://github.com/user-attachments/files/32935156/final-presentation.html)[Uploading fin<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>StreamLine Spotlight, A Personalised Discovery Rail</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Saans:wght@400;600;700;800;900&family=Antarctican+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{--bg:#07162C;--fg:#fff;--or:#fb923c;--cy:#22d3ee;--tl:#34d399;--bl:#60a5fa;--vi:#a78bfa;--pk:#f472b6;--bd:rgba(251,146,60,.25)}
*{box-sizing:border-box;margin:0}
html{scroll-snap-type:y mandatory;scroll-behavior:smooth;background:var(--bg)}
body{background:var(--bg);color:var(--fg);font-family:'Saans','Helvetica Neue',Arial,sans-serif;font-weight:400;line-height:1.5}
h1,h2,h3{font-weight:800;line-height:1.1;letter-spacing:-.01em}
section{min-height:100vh;scroll-snap-align:start;padding:6vh 8vw;display:flex;flex-direction:column;justify-content:center;gap:2.2vh;position:relative}
.eb,.mono{font-family:'Antarctican Mono',ui-monospace,Menlo,monospace}
.eb{text-transform:uppercase;letter-spacing:.12em;color:#fdba74;font-size:.8rem;font-weight:500}
h2{font-size:clamp(1.8rem,3.6vw,3rem);font-weight:900}
h1{font-size:clamp(2.4rem,5.4vw,4.6rem);font-weight:900}
.or{color:var(--or)}
.lead{font-size:clamp(1rem,1.5vw,1.3rem);max-width:60ch}
.card{background:rgba(255,255,255,.04);border:1px solid var(--bd);border-radius:15px;padding:1.3rem 1.5rem}
.hero{background:linear-gradient(135deg,rgba(251,146,60,.18),rgba(34,211,238,.07));box-shadow:0 14px 40px rgba(0,0,0,.45)}
.grid{display:grid;gap:1.2rem}.g2{grid-template-columns:1fr 1fr}.g3{grid-template-columns:repeat(3,1fr)}.g4{grid-template-columns:repeat(4,1fr)}
.card h3{font-size:1.1rem;margin-bottom:.4rem}
.card p,.card li{font-size:.98rem}
.lab{font-family:'Antarctican Mono',monospace;font-size:.72rem;text-transform:uppercase;letter-spacing:.12em;margin-bottom:.4rem;display:block}
.callout{border-left:4px solid var(--or);background:rgba(251,146,60,.12);border-radius:0 15px 15px 0;padding:1.2rem 1.5rem;font-size:clamp(1rem,1.5vw,1.25rem);font-weight:600}
.bad{border-left-color:var(--pk);background:rgba(244,114,182,.12)}
.pill{display:inline-block;border:1px solid var(--bd);border-radius:99px;padding:.3rem .9rem;font-family:'Antarctican Mono',monospace;font-size:.8rem;margin:0 .4rem .4rem 0}
.btn{display:inline-block;background:var(--or);color:#07162C;font-weight:800;text-decoration:none;padding:.8rem 1.5rem;border-radius:12px;box-shadow:0 8px 24px rgba(251,146,60,.35)}
.btn:hover{filter:brightness(1.1)}
a{color:var(--cy);word-break:break-all}
.journey{display:flex;gap:.8rem;align-items:stretch}
.step{flex:1;text-align:center;padding:1rem;border-radius:14px;border:1px solid var(--bd);background:rgba(255,255,255,.04);font-weight:700}
.step.mis{background:rgba(244,114,182,.18);border-color:var(--pk);box-shadow:0 0 0 2px rgba(244,114,182,.3)}
.step small{display:block;font-family:'Antarctican Mono',monospace;font-weight:400;font-size:.7rem;color:#fdba74;margin-top:.3rem}
ul{padding-left:1.1rem}
#bar{position:fixed;top:0;left:0;height:4px;width:0;background:linear-gradient(90deg,var(--or),var(--cy));z-index:10}
#dots{position:fixed;right:1.2vw;top:50%;transform:translateY(-50%);display:flex;flex-direction:column;gap:.7rem;z-index:10}
#dots a{width:10px;height:10px;border-radius:50%;background:rgba(255,255,255,.3);display:block}
#dots a.on{background:var(--or);transform:scale(1.4)}
.rule{display:grid;grid-template-columns:auto 1fr;gap:.2rem .8rem;font-size:.98rem}
@media(max-width:800px){.g2,.g3,.g4{grid-template-columns:1fr}.journey{flex-direction:column}}
</style>
</head>
<body>
<div id="bar"></div>
<nav id="dots" aria-label="Slides"></nav>

<section id="s0">
  <span class="eb">Product School · PM Certification · Final Project</span>
  <h1>StreamLine Spotlight,<br><span class="or">A Personalised Discovery Rail</span></h1>
  <p class="lead">Turn an overwhelming home screen into 30-minute listening sessions with a Spotlight rail that tells each Explorer why they will love a title.</p>
  <div class="grid g2" style="max-width:900px">
    <div class="card hero"><span class="lab" style="color:#fdba74">Presented by</span>Sahana Parameswarappa · Product Management Cohort · Jun 2026</div>
    <div class="card"><span class="lab" style="color:var(--cy)">Repo</span><a href="https://github.com/SahanaVeer/pm-final-project/tree/main">github.com/SahanaVeer/pm-final-project</a></div>
  </div>
  <div><a class="btn" href="https://lovable.dev/projects/356b9207-61f6-4c57-b675-599cdd606953" target="_blank" rel="noopener">View prototype →</a></div>
</section>

<section id="s1">
  <span class="eb">Slide 5 · Strategy</span>
  <h2>Problem hook</h2>
  <p class="lead">Casual Explorers open StreamLine to unwind but bounce from a generic, algorithm-only home screen. "Nothing to play" is the #1 reason cited for short, sub-10-minute sessions.</p>
  <div class="card hero"><span class="lab" style="color:var(--or)">Value proposition</span><p>Spotlight reframes discovery from endless scrolling into a curated, reasoned shortlist, six titles, each with a one-line "why you will love this" so the choice feels effortless.</p></div>
  <div class="callout"><span class="lab" style="color:#fdba74">Data-backed hypothesis</span>We believe a personalised Spotlight rail for Casual Explorers will increase the share of 30-minute sessions started from discovery, measured by a +2pt lift within 14 days, without hurting 7-day retention.</div>
</section>

<section id="s2">
  <span class="eb">Slide 6 · Research</span>
  <h2>Competitive analysis &amp; workaround</h2>
  <div class="grid g2">
    <div class="card"><span class="lab" style="color:var(--bl)">Workaround</span><p>Today Explorers cope by leaving to TikTok / YouTube for recommendations, then returning to StreamLine to search manually.</p></div>
    <div class="card"><span class="lab" style="color:var(--vi)">Competitors</span><p>Netflix "Top Picks" and Spotify "Made For You" both frame recommendations with an explicit reason; StreamLine surfaces titles with no rationale.</p></div>
  </div>
  <span class="eb">Journey map</span>
  <div class="journey">
    <div class="step">Open app</div>
    <div class="step">Scan three generic rows</div>
    <div class="step mis">Hesitate<small>Moment of misery</small></div>
    <div class="step">Bounce</div>
  </div>
  <div class="callout">Spotlight inserts a reasoned shortlist exactly at the hesitation point, before the user gives up.</div>
</section>

<section id="s3">
  <span class="eb">Slide 7 · Blueprint</span>
  <h2>Prioritisation &amp; PRD</h2>
  <div class="grid g4">
    <div class="card hero"><span class="lab" style="color:var(--or)">Must</span><p>Pinned Spotlight rail + "why you will love this" reason.</p></div>
    <div class="card"><span class="lab" style="color:var(--tl)">Should</span><p>Taste-profile tuning controls.</p></div>
    <div class="card"><span class="lab" style="color:var(--cy)">Could</span><p>Social-proof badges.</p></div>
    <div class="card"><span class="lab" style="color:var(--pk)">Won't (now)</span><p>Full home-screen redesign.</p></div>
  </div>
  <p class="lead">Now/Next/Later roadmap ships a V1 rail in 6 weeks.</p>
  <div class="card"><span class="lab" style="color:#fdba74">PRD highlights</span><ul><li>A pinned top rail of 6 personalised titles, each with a single AI-generated one-line reason.</li><li>No other home-screen changes in V1.</li><li>Falls back to the existing editorial row if the taste profile is empty.</li></ul></div>
  <div><a class="btn" href="https://lovable.dev/projects/356b9207-61f6-4c57-b675-599cdd606953" target="_blank" rel="noopener">View prototype →</a></div>
</section>

<section id="s4">
  <span class="eb">Slide 8 · Validation</span>
  <h2>Experiment plan</h2>
  <div class="card hero">
    <span class="lab" style="color:var(--or)">A/B test · 50/50 split · 14 days</span>
    <div class="grid g2">
      <div><h3>Control</h3><p>Existing home screen.</p></div>
      <div><h3>Variant</h3><p>Home screen with the pinned Spotlight rail.</p></div>
    </div>
  </div>
  <div class="grid g2">
    <div class="card"><span class="lab" style="color:var(--cy)">Primary metric</span><p>Share of 30-minute sessions started from discovery.</p><p class="mono" style="color:var(--or);margin-top:.4rem">Baseline 11% · MDE +2pt</p></div>
    <div class="card"><span class="lab" style="color:var(--pk)">Guardrail</span><p>7-day retention must not drop more than 2pt.</p></div>
  </div>
  <div class="card"><span class="lab" style="color:#fdba74">Decision rules</span>
    <div class="rule"><b class="or">Ship</b><span>if primary hits with guardrail safe</span><b style="color:var(--cy)">Iterate</b><span>if flat</span><b style="color:var(--pk)">Kill</b><span>if retention regresses</span></div></div>
</section>

<section id="s5">
  <span class="eb">Slide 9 · Launch</span>
  <h2>GTM &amp; success metrics</h2>
  <div class="grid g2">
    <div class="card hero">
      <span class="lab" style="color:var(--or)">GTM strategy</span>
      <p><b>Goal:</b> engagement</p>
      <p><b>Audience:</b> existing Casual Explorers who have not adopted discovery</p>
      <p><b>Tier:</b> M (medium)</p>
      <p style="margin:.6rem 0"><span class="pill">In-app announcement (owned)</span><span class="pill">Lifecycle email (owned)</span><span class="pill">Lifecycle push</span></p>
      <p><b>Enablement:</b> a support macro + a changelog entry</p>
    </div>
    <div class="card">
      <span class="lab" style="color:var(--tl)">Success metrics</span>
      <ul><li>Feature adoption rate</li><li>30-minute discovery sessions</li><li>Time-to-first-play</li></ul>
    </div>
  </div>
  <div class="callout bad"><span class="lab" style="color:var(--pk)">Bad signal</span>Adoption rises but 7-day retention stays flat, that means novelty, not durable value.</div>
</section>

<section id="s6">
  <span class="eb">Slide 10 · Story</span>
  <h2>Friction, aha &amp; what's next</h2>
  <div class="grid g2">
    <div class="card hero"><span class="lab" style="color:var(--or)">Friction + aha moment</span><p>Writing the one-line "why you will love this" reason forced real clarity on the persona, the aha moment was realising the reason copy, not the algorithm, was the product. The hardest part was resisting the urge to redesign the whole home screen.</p></div>
    <div class="card"><span class="lab" style="color:var(--cy)">Key takeaways / next</span><p>Biggest takeaway: a tight, reasoned shortlist beats a longer list. Next I would close the loop, feed Spotlight engagement back into the taste model and A/B test social-proof badges.</p></div>
  </div>
</section>

<section id="s7" style="text-align:center;align-items:center">
  <span class="eb">Thank you</span>
  <h1>Thank <span class="or">you</span></h1>
  <p class="lead"><a href="https://github.com/SahanaVeer/pm-final-project/tree/main">https://github.com/SahanaVeer/pm-final-project/tree/main</a></p>
  <p><span class="pill">Product Management Cohort · Jun 2026</span></p>
  <div class="callout" style="border-radius:99px;border-left-width:1px;border:1px solid var(--or);padding:.8rem 2rem">Submit to the learning platform</div>
</section>

<script>
(function(){
  var s=[].slice.call(document.querySelectorAll('section')),d=document.getElementById('dots'),b=document.getElementById('bar');
  s.forEach(function(e,i){var a=document.createElement('a');a.href='#'+e.id;a.setAttribute('aria-label','Slide '+(i+1));d.appendChild(a)});
  var dots=d.children;
  function cur(){var y=window.scrollY+innerHeight/2,c=0;s.forEach(function(e,i){if(e.offsetTop<=y)c=i});return c}
  function upd(){var m=document.documentElement.scrollHeight-innerHeight;b.style.width=(m>0?scrollY/m*100:0)+'%';var c=cur();for(var i=0;i<dots.length;i++)dots[i].className=i==c?'on':''}
  function go(i){s[Math.max(0,Math.min(s.length-1,i))].scrollIntoView({behavior:'smooth'})}
  addEventListener('scroll',upd,{passive:true});addEventListener('resize',upd);upd();
  addEventListener('keydown',function(e){
    var k=e.key;
    if(k=='ArrowDown'||k==' '||k=='PageDown'){e.preventDefault();go(cur()+(e.shiftKey&&k==' '?-1:1))}
    else if(k=='ArrowUp'||k=='PageUp'){e.preventDefault();go(cur()-1)}
    else if(k=='Home'){e.preventDefault();go(0)}
    else if(k=='End'){e.preventDefault();go(s.length-1)}
    else if(k=='Escape'){go(0)}
  });
})();
</script>
</body>
</html>
al-presentation.html…]()
