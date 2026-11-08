# weclean-website<!DOCTYPE html>
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
  --fb:#1877F2;
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
.nav-in{display:flex;align-items:center;justify-content:space-between;height:74px;gap:10px}
.brand{display:flex;flex-direction:column;flex-shrink:0}
.brand b{font-size:17px;color:var(--blue);font-weight:900;line-height:1.2}
.brand span{font-size:11px;color:var(--muted);white-space:nowrap}
.nav-links{display:flex;gap:18px;align-items:center}
.nav-links a{font-size:14px;font-weight:500;color:var(--body);transition:.2s}
.nav-links a:hover{color:var(--blue)}
.nav-cta{display:flex;align-items:center;gap:6px;flex-shrink:0}
.btn{
  display:inline-flex;align-items:center;justify-content:center;gap:5px;
  padding:8px 12px;border-radius:999px;font-weight:700;font-size:13px;border:none;cursor:pointer;transition:.2s;white-space:nowrap;
}
.btn-wa{background:var(--wa);color:#fff}
.btn-wa:hover{opacity:.9}
.btn-primary{background:var(--blue);color:#fff}
.btn-primary:hover{background:var(--blue-dark)}
.btn-fb{background:var(--fb);color:#fff}
.btn-ig{background:radial-gradient(circle at 30% 107%, #fdf497 0%, #df3484 45%, #7624cb 90%);color:#fff}

/* ============ HERO ============ */
.hero{
  padding:130px 0 80px;
  background:radial-gradient(1000px 500px at 90% 0%, rgba(156,203,74,.12), transparent 60%), linear-gradient(180deg,var(--blue-softer) 0%,#fff 100%);
}
.hero-grid{display:grid;grid-template-columns:1.1fr .9fr;gap:50px;align-items:center}
.badge-top{
  display:inline-flex;gap:8px;align-items:center;background:#fff;border:1px solid var(--line);
  padding:6px 14px;border-radius:999px;font-size:13px;font-weight:700;color:var(--blue);margin-bottom:20px;
}
.pulse{width:8px;height:8px;background:var(--green);border-radius:50%;animation:pulse 2s infinite}
@keyframes pulse{70%{box-shadow:0 0 0 8px rgba(156,203,74,0)}100%{box-shadow:0 0 0 0 rgba(156,203,74,0)}}
.hero h1{font-size:clamp(30px,4.2vw,48px);margin-bottom:18px}
.hero h1 span{color:var(--blue)}
.hero p{font-size:17px;margin-bottom:28px;color:var(--body)}
.hero-btns{display:flex;gap:10px;flex-wrap:wrap}

/* 社會信任按鈕列 */
.social-proof-bar{display:flex;gap:10px;margin-top:20px;flex-wrap:wrap}
.social-btn{
  display:inline-flex;align-items:center;gap:8px;padding:8px 16px;border-radius:999px;
  font-size:13.5px;font-weight:700;color:#fff;box-shadow:var(--shadow-sm);transition:.2s;
}
.social-btn.fb{background:var(--fb)}
.social-btn.ig{background:linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888)}
.social-btn:hover{transform:translateY(-2px);opacity:.9}

/* 核心保證條 */
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

/* ============ 屋苑實拍紀錄 ============ */
.works-sec{background:var(--blue-softer)}
.works-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:20px}
.work-card{background:#fff;border-radius:var(--r);overflow:hidden;border:1px solid var(--line);box-shadow:var(--shadow-sm)}
.work-card img{width:100%;height:220px;object-fit:cover}
.work-info{padding:16px}
.work-info b{display:block;font-size:16px;color:var(--ink);margin-bottom:4px}
.work-info span{font-size:13px;color:var(--muted)}

/* ============ 報價器 ============ */
.quote-sec{background:#fff}
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

/* ============ 頁腳 ============ */
footer{background:#0D2136;color:#9FB4C8;padding:40px 0 20px;font-size:13.5px;text-align:center}
footer p{margin-bottom:10px;color:#fff}
.footer-socials{display:flex;justify-content:center;gap:15px
