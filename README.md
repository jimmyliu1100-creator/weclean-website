# weclean-website

<!DOCTYPE html>
<html lang="zh-HK">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Weclean 專業清潔及冷氣清洗服務 | 24小時服務 港九新界 無隱藏式收費</title>
<meta name="description" content="Weclean 專業冷氣深層清洗、A/B計劃、家居清潔與滅蟲服務。24小時服務，港九新界18區全覆蓋，明碼實價，無隱藏式收費。">
<link rel="icon" href="assets/logo_icon.png">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@400;500;700;900&display=swap" rel="stylesheet">
<style>
:root{
  --blue:#0F5FA6;
  --blue-dark:#0A4780;
  --blue-light:#1B7CC9;
  --blue-pale:#EAF4FC;
  --blue-softer:#F5FAFE;
  --green:#9CCB4A;
  --green-dark:#7BB32F;
  --ink:#16283D;
  --body:#3E5266;
  --muted:#6B8098;
  --line:#DCE8F3;
  --white:#fff;
  --shadow-sm:0 2px 8px rgba(15,95,166,.07);
  --shadow:0 8px 28px rgba(15,95,166,.11);
  --shadow-lg:0 18px 50px rgba(15,95,166,.16);
  --r:16px; --r-lg:24px;
  --wa:#25D366;
}
*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth;-webkit-text-size-adjust:100%}
body{
  font-family:"Noto Sans TC","PingFang HK","Microsoft JhengHei",sans-serif;
  color:var(--body); line-height:1.75; background:var(--white); font-size:16px; overflow-x:hidden;
}
img{max-width:100%;display:block}
a{color:inherit;text-decoration:none}
.wrap{width:min(1200px,92vw);margin:0 auto}
section{padding:80px 0}
h1,h2,h3{color:var(--ink);line-height:1.3;font-weight:900}

/* ============ 導航 ============ */
.nav{
  position:fixed;top:0;left:0;right:0;z-index:200;
  background:rgba(255,255,255,.95);backdrop-filter:blur(14px);
  border-bottom:1px solid var(--line);
}
.nav-in{display:flex;align-items:center;justify-content:space-between;height:74px}
.brand b{font-size:20px;color:var(--blue);font-weight:900}
.brand span{display:block;font-size:11px;color:var(--muted)}
.nav-links{display:flex;gap:24px;align-items:center}
.nav-links a{font-size:15px;font-weight:500;color:var(--body);transition:.2s}
.nav-links a:hover{color:var(--blue)}
.nav-cta{display:flex;align-items:center;gap:12px}
.btn{
  display:inline-flex;align-items:center;justify-content:center;gap:8px;
  padding:11px 20px;border-radius:999px;font-weight:700;font-size:14px;border:none;cursor:pointer;transition:.2s;
}
.btn-wa{background:var(--wa);color:#fff}
.btn-wa:hover{opacity:.9}
.btn-primary{background:var(--blue);color:#fff}
.btn-primary:hover{background:var(--blue-dark)}
.nav-toggle{display:none;background:none;border:none;font-size:24px;cursor:pointer}

/* ============ HERO ============ */
.hero{
  padding:140px 0 80px;
  background:radial-gradient(1000px 500px at 90% 0%, rgba(156,203,74,.12), transparent 60%), linear-gradient(180deg,var(--blue-softer) 0%,#fff 100%);
}
.hero-grid{display:grid;grid-template-columns:1.1fr .9fr;gap:50px;align-items:center}
.badge-top{
  display:inline-flex;gap:8px;align-items:center;background:#fff;border:1px solid var(--line);
  padding:6px 14px;border-radius:999px;font-size:13px;font-weight:700;color:var(--blue);margin-bottom:20px;
}
.pulse{width:8px;height:8px;background:var(--green);border-radius:50%;animation:pulse 2s infinite}
@keyframes pulse{70%{box-shadow:0 0 0 8px rgba(156,203,74,0)}100%{box-shadow:0 0 0 0 rgba(156,203,74,0)}}
.hero h1{font-size:clamp(32px,4.5vw,48px);margin-bottom:18px}
.hero h1 span{color:var(--blue)}
.hero p{font-size:17px;margin-bottom:28px;color:var(--body)}
.hero-btns{display:flex;gap:12px;flex-wrap:wrap}

/* 亮點特色條 */
.core-features{background:var(--blue);color:#fff;padding:28px 0}
.cf-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;text-align:center}
.cf-item b{display:block;font-size:22px;color:var(--green);font-weight:900}
.cf-item span{font-size:14px;opacity:.95}

/* ============ 服務與計劃 ============ */
.sec-head{text-align:center;max-width:680px;margin:0 auto 46px}
.sec-tag{background:var(--blue-pale);color:var(--blue);padding:6px 16px;border-radius:999px;font-size:12px;font-weight:700;display:inline-block;margin-bottom:12px}
.sec-head h2{font-size:clamp(26px,3vw,34px);margin-bottom:10px}

.srv-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(340px,1fr));gap:24px}
.srv-card{background:#fff;border:1px solid var(--line);border-radius:var(--r);padding:32px;box-shadow:var(--shadow-sm);transition:.2s}
.srv-card:hover{box-shadow:var(--shadow);transform:translateY(-4px)}
.srv-card.featured{border:2px solid var(--blue-light)}
.srv-card h3{font-size:20px;margin-bottom:10px;color:var(--ink)}
.srv-card p{font-size:14.5px;color:var(--muted);margin-bottom:18px}
.price-list{background:var(--blue-softer);border-radius:var(--r-sm);padding:14px;font-size:14px;margin-top:14px}
.price-list b{display:block;color:var(--blue-dark);margin-bottom:6px}

/* ============ 報價器 ============ */
.quote-sec{background:var(--blue-softer)}
.quote-box{background:#fff;border-radius:var(--r-lg);box-shadow:var(--shadow);border:1px solid var(--line);display:grid;grid-template-columns:1fr 1fr;overflow:hidden}
.q-form{padding:36px}
.q-sum{background:var(--blue);color:#fff;padding:36px;display:flex;flex-direction:column}
.field{margin-bottom:20px}
.field label{display:block;font-weight:700;font-size:14px;margin-bottom:8px}
.field select{width:100%;padding:12px;border:1.5px solid var(--line);border-radius:8px;font-size:15px;background:#fff}
.chips{display:flex;flex-wrap:wrap;gap:8px}
.chip{padding:8px 16px;border:1.5px solid var(--line);border-radius:999px;background:#fff;font-size:14px;cursor:pointer;user-select:none}
.chip.on{background:var(--blue);color:#fff;border-color:var(--blue);font-weight:700}
.q-line{display:flex;justify-content:space-between;padding:10px 0;border-bottom:1px solid rgba(255,255,255,.15);font-size:15px}
.q-line.total{margin-top:auto;border-top:2px solid rgba(255,255,255,.3);border-bottom:none;padding-top:16px}
.q-line.total b{font-size:28px;color:var(--green)}

/* ============ 頁腳 ============ {*/
footer{background:#0D2136;color:#9FB4C8;padding:40px 0 20px;font-size:13.5px;text-align:center}
footer p{margin-bottom:10px;color:#fff}

@media(max-width:900px){
  .hero-grid{grid-template-columns:1fr;text-align:center}
  .hero-btns{justify-content:center}
  .quote-box{grid-template-columns:1fr}
  .cf-grid{grid-template-columns:1fr;gap:12px}
  .nav-links{display:none}
  .nav-toggle{display:block}
}
</style>
</head>
<body>

<!-- 導航 -->
<nav class="nav">
  <div class="wrap nav-in">
    <div class="brand">
      <b>WeClean 專業清潔</b>
      <span>24小時 · 港九新界</span>
    </div>
    <div class="nav-links">
      <a href="#services">服務項目</a>
      <a href="#quote">即時報價</a>
      <a href="#faq">常見問題</a>
    </div>
    <div class="nav-cta">
      <a href="tel:+85262572787" class="btn btn-primary">📞 6257 2787</a>
      <a href="https://wa.me/85262572787?text=%E4%BD%A0%E5%A5%BD%EF%BC%8C%E6%88%91%E6%83%B3%E6%9F%A5%E8%A9%A2Weclean%E6%9C%8D%E5%8B%99" target="_blank" rel="noopener" class="btn btn-wa">WhatsApp</a>
    </div>
  </div>
</nav>

<!-- HERO -->
<header class="hero">
  <div class="wrap hero-grid">
    <div>
      <div class="badge-top"><span class="pulse"></span> 24小時服務 ｜ 港九新界 18區全覆蓋</div>
      <h1>專業冷氣清洗與<br><span>全方位家居清潔服務</span></h1>
      <p>明碼實價，<strong>無隱藏式收費</strong>。提供冷氣 A/B 雙計劃深層清洗、家居清潔、除甲醛及長效滅蟲，隨時預約，即日上門。</p>
      <div class="hero-btns">
        <a href="#quote" class="btn btn-primary btn-lg">⚡ 立即取得報價</a>
        <a href="https://wa.me/85262572787?text=%E4%BD%A0%E5%A5%BD%EF%BC%8C%E6%88%91%E6%83%B3%E6%9F%A5%E8%A9%A2Weclean%E6%9C%8D%E5%8B%99" target="_blank" rel="noopener" class="btn btn-wa btn-lg">💬 WhatsApp 查詢</a>
      </div>
    </div>
    <div>
      <div class="hero-photo" style="border-radius:var(--r-lg);overflow:hidden;box-shadow:var(--shadow-lg);">
        <img src="assets/work_grandview.jpg" alt="Weclean 專業上門服務">
      </div>
    </div>
  </div>
</header>

<!-- 核心保證條 -->
<div class="core-features">
  <div class="wrap cf-grid">
    <div class="cf-item"><b>⏱️ 24小時服務</b><span>全天候隨時預約，即日可約</span></div>
    <div class="cf-item"><b>📍 港九新界</b><span>18區全覆蓋，上門準時</span></div>
    <div class="cf-item"><b>🛡️ 無隱藏式收費</b><span>明碼實價，$0小費保證</span></div>
  </div>
</div>

<!-- 服務項目 -->
<section id="services">
  <div class="wrap">
    <div class="sec-head">
      <span class="sec-tag">OUR SERVICES</span>
      <h2>精選皇牌服務與明碼實價</h2>
      <p>清晰透明的收費標準，滿足你對家居潔淨的所有需求</p>
    </div>
    <div class="srv-grid">
      <div class="srv-card featured">
        <h3>❄️ 冷氣機深層清洗（A/B計劃）</h3>
        <p>全拆式高壓清洗，徹底去除霉菌與異味。</p>
        <div class="price-list">
          <b>A計劃（深層清洗＋消毒）：</b>
          1部 $680 ｜ 2部 $1,080 ｜ 3部 $1,250 ｜ 4部 $1,500 ｜ 5部 $1,750 ｜ 6部 $2,000<br><br>
          <b>B計劃（深層清洗＋消毒＋銀離子防霉塗層，維持約1年）：</b>
          1部 $730 ｜ 2部 $1,200 ｜ 3部 $1,500 ｜ 4部 $1,850 ｜ 5部 $2,050 ｜ 6部 $2,300
        </div>
      </div>
      <div class="srv-card">
        <h3>🏠 家居清潔與除甲醛</h3>
        <p>全屋深層清潔、入伙前後執整及專業光觸媒除甲醛服務，讓新居空氣清新，母嬰安心。</p>
      </div>
      <div class="srv-card">
        <h3>🐜 家居滅蟲與床褥梳化清洗</h3>
        <p>高效微米級噴霧滅蟲（曱甴、木蝨等）及 Karcher 高溫蒸氣除蟎，守護全家健康。</p>
      </div>
    </div>
  </div>
</section>

<!-- 即時報價 -->
<section class="quote-sec" id="quote">
  <div class="wrap">
    <div class="sec-head">
      <span class="sec-tag">INSTANT QUOTE</span>
      <h2>即時報價計算器</h2>
      <p>選定方案與數量，30秒即時知道參考價錢</p>
    </div>
    <div class="quote-box">
      <div class="q-form">
        <div class="field">
          <label>選擇冷氣清洗計劃</label>
          <select id="planType">
            <option value="planA">A計劃（深層清洗＋消毒）</option>
            <option value="planB">B計劃（深層清洗＋銀離子防霉保約一年）</option>
          </select>
        </div>
        <div class="field">
          <label>冷氣機數量</label>
          <div class="chips" id="acChips">
            <div class="chip on" data-v="1">1 部</div>
            <div class="chip" data-v="2">2 部</div>
            <div class="chip" data-v="3">3 部</div>
            <div class="chip" data-v="4">4 部</div>
            <div class="chip" data-v="5">5 部</div>
            <div class="chip" data-v="6">6 部</div>
          </div>
        </div>
        <div class="field">
          <label>附加服務（可多選）</label>
          <div class="chips" id="addChips">
            <div class="chip" data-v="80" data-name="室外機清洗">室外機清洗 ($80)</div>
            <div class="chip" data-v="280" data-name="浴室寶/抽氣扇">浴室寶/抽氣扇 ($280)</div>
            <div class="chip" data-v="150" data-name="清洗洗衣機">清洗洗衣機 ($150)</div>
            <div class="chip" data-v="350" data-name="廚房抽風扇">廚房抽風扇 ($350)</div>
          </div>
        </div>
        <div class="field">
          <label>地區選擇</label>
          <select id="area">
            <option value="0">九龍 / 新界 / 其他地區（免隧道費）</option>
            <option value="60">港島區（含隧道附加費 +$60）</option>
          </select>
        </div>
      </div>
      <div class="q-sum">
        <h3>📋 你的報價單</h3>
        <div id="qLines" style="margin:20px 0"></div>
        <div style="font-size:12px;opacity:.8;margin-bottom:20px">✨ 24小時服務 ｜ 港九新界 ｜ 無隱藏式收費</div>
        <a href="#" id="waBtn" target="_blank" rel="noopener" class="btn btn-wa btn-lg" style="background:#fff;color:var(--wa);width:100%;text-align:center;justify-content:center">💬 立即 WhatsApp 預約</a>
      </div>
    </div>
  </div>
</section>

<!-- 頁腳 -->
<footer>
  <div class="wrap">
    <p><strong>Weclean 專業清潔及冷氣清洗服務</strong></p>
    <p>24小時服務 ｜ 港九新界 18區全覆蓋 ｜ 無隱藏式收費</p>
    <p style="font-size:12px;opacity:.7;margin-top:15px">© 2026 Weclean. All Rights Reserved.</p>
  </div>
</footer>

<script>
const PLAN_TYPE=document.getElementById('planType');
const AC_CHIPS=document.getElementById('acChips');
const ADD_CHIPS=document.getElementById('addChips');
const AREA=document.getElementById('area');
const QLINES=document.getElementById('qLines');
const WA_BTN=document.getElementById('waBtn');

const PRICES={
  planA: { 1: 680, 2: 1080, 3: 1250, 4: 1500, 5: 1750, 6: 2000 },
  planB: { 1: 730, 2: 1200, 3: 1500, 4: 1850, 5: 2050, 6: 2300 }
};

function bindChips(container,isMulti){
  container.querySelectorAll('.chip').forEach(c=>{
    c.addEventListener('click',()=>{
      if(isMulti){ c.classList.toggle('on'); }
      else{ container.querySelectorAll('.chip').forEach(x=>x.classList.remove('on')); c.classList.add('on'); }
      update();
    });
  });
}
bindChips(AC_CHIPS,false);
bindChips(ADD_CHIPS,true);
PLAN_TYPE.addEventListener('change',update);
AREA.addEventListener('change',update);

function update(){
  const plan=PLAN_TYPE.value;
  const qty=[...AC_CHIPS.querySelectorAll('.chip.on')][0]?.dataset.v || 1;
  const base=PRICES[plan][qty];
  const addons=[...ADD_CHIPS.querySelectorAll('.chip.on')].map(c=>({price:parseInt(c.dataset.v),name:c.dataset.name}));
  const addTotal=addons.reduce((s,a)=>s+a.price,0);
  const tunnel=parseInt(AREA.value);
  const total=base+addTotal+tunnel;

  let html=`<div class="q-line"><span>${plan==='planB'?'B計劃（銀離子防霉）':'A計劃（深層清洗）'} × ${qty}部</span><b>$${base}</b></div>`;
  addons.forEach(a=>html+=`<div class="q-line"><span>${a.name}</span><b>$${a.price}</b></div>`);
  if(tunnel>0) html+=`<div class="q-line"><span>港島隧道費</span><b>$${tunnel}</b></div>`;
  html+=`<div class="q-line total"><span>參考總價</span><b>$${total}</b></div>`;
  QLINES.innerHTML=html;

  const msg=`你好，我想預約 Weclean 服務：\n• 方案：${plan==='planB'?'B計劃':'A計劃'} × ${qty}部\n• 參考總價：$${total}\n請幫手安排！`;
  WA_BTN.href=`https://wa.me/85262572787?text=${encodeURIComponent(msg)}`;
}
update();
</script>
</body>
</html>
