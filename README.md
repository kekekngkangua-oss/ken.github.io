<!DOCTYPE html><html lang="en"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover"><title>My Daily Activity</title>
<style>
:root{color-scheme:dark;--bg:#030712;--bd:#1f3070;--tx:#e8ecff;--mut:#8fa0d6;--a:#4d7bff;--b:#a855f7;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
*{box-sizing:border-box}html{scroll-behavior:smooth;scroll-padding-top:90px}
body{margin:0;background:var(--bg);color:var(--tx);font-family:Inter,system-ui,-apple-system,"Segoe UI",sans-serif;line-height:1.6;overflow-x:hidden}
#stars{position:fixed;inset:0;z-index:-1;width:100%;height:100%}
.glow{position:fixed;width:340px;height:340px;border-radius:50%;background:radial-gradient(#4d7bff44,transparent 70%);pointer-events:none;z-index:-1;transform:translate(-50%,-50%);left:50%;top:30%}
#bar{position:fixed;top:0;left:0;height:3px;width:0;background:linear-gradient(90deg,var(--a),var(--b));z-index:9}
nav{position:sticky;top:env(safe-area-inset-top,0px);z-index:5;display:flex;gap:4px;width:max-content;max-width:94%;margin:14px auto 0;padding:6px;border:1px solid var(--bd);border-radius:999px;background:#050b22cc;backdrop-filter:blur(12px)}
nav a{color:var(--tx);text-decoration:none;font-weight:600;font-size:.88rem;padding:8px 15px;border-radius:999px;transition:.25s}nav a:hover,nav a.on{background:#17338a}
main{max-width:780px;margin:0 auto;padding:0 20px 40px}
.hero{padding:60px 0 24px}.pill{display:inline-flex;gap:8px;align-items:center;border:1px solid var(--bd);background:#0a1438;border-radius:999px;padding:6px 14px;font-size:.85rem;color:#b8c6ff}
.pill i{width:8px;height:8px;border-radius:50%;background:#22d3a0;box-shadow:0 0 10px #22d3a0;animation:p 1.6s infinite}@keyframes p{50%{opacity:.3}}
.hero h1{font-size:clamp(2.6rem,11vw,4.4rem);line-height:1.05;margin:18px 0 14px;letter-spacing:-.03em}
.grad{background:linear-gradient(90deg,#6c8dff,#c084fc,#6c8dff);background-size:200%;-webkit-background-clip:text;background-clip:text;color:transparent;animation:g 5s linear infinite}@keyframes g{to{background-position:200%}}
.sub{font-weight:600;font-size:1.15rem;min-height:1.8em}#t::after{content:"|";animation:b 1s steps(1) infinite}@keyframes b{50%{opacity:0}}
.hero p{color:#c3cdf0;max-width:560px}
.btn{display:inline-block;margin:6px 8px 0 0;background:linear-gradient(135deg,var(--a),var(--b));color:#fff;padding:12px 22px;border-radius:12px;font-weight:600;text-decoration:none;box-shadow:0 0 34px #4d7bff55;transition:.25s}.btn:hover{transform:translateY(-2px)}
.btn.o{background:transparent;border:1px solid var(--bd);box-shadow:none}
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin:34px 0}
.st{border:1px solid var(--bd);background:#0a1231aa;border-radius:16px;padding:16px;text-align:center;backdrop-filter:blur(6px)}
.st b{display:block;font-size:1.9rem;background:linear-gradient(90deg,#6c8dff,#c084fc);-webkit-background-clip:text;background-clip:text;color:transparent}.st span{color:var(--mut);font-size:.82rem}
h2{font-size:1.7rem;margin:30px 0 4px}.lead{color:var(--mut);margin:0 0 16px}
.chips{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:26px}
.chip{border:1px solid var(--bd);background:#0a1231;color:var(--tx);padding:8px 16px;border-radius:999px;font:600 .85rem inherit;cursor:pointer;transition:.25s}
.chip.on{background:linear-gradient(135deg,var(--a),var(--b));border-color:transparent}
.tl{position:relative;padding-left:34px}.tl::before{content:"";position:absolute;left:11px;top:6px;bottom:6px;width:2px;background:linear-gradient(var(--a),var(--b),transparent)}
.card{position:relative;margin-bottom:28px;border:1px solid var(--bd);border-radius:22px;background:linear-gradient(180deg,#0c1840cc,#070d25cc);overflow:hidden;transition:transform .2s,box-shadow .3s;transform-style:preserve-3d}
.card:hover{box-shadow:0 18px 50px #4d7bff30;border-color:#3555c0}
.card::before{content:"";position:absolute;left:-30px;top:26px;width:14px;height:14px;border-radius:50%;background:var(--a);box-shadow:0 0 0 5px #4d7bff30,0 0 18px var(--a)}
.card.hide{display:none}
.ph{position:relative;background:#050a1e;display:flex;justify-content:center;min-height:56px}
.ph img{width:100%;height:auto;max-height:80vh;object-fit:contain;display:block;cursor:zoom-in}
.time{position:absolute;left:12px;top:12px;font-family:ui-monospace,Menlo,monospace;font-size:.85rem;background:#030712cc;border:1px solid var(--bd);padding:4px 12px;border-radius:999px;backdrop-filter:blur(6px)}
.tx{padding:16px 20px 22px;position:relative}.tx h3{margin:0 0 4px;font-size:1.3rem}.tx p{margin:0;color:#b9c4ec}
.n{position:absolute;right:18px;top:8px;font-size:2.4rem;font-weight:800;color:#18285e}
.card.now{border-color:#22d3a0}.card.now::after{content:"NOW";position:absolute;right:12px;top:12px;background:#22d3a0;color:#032;font-weight:800;font-size:.7rem;padding:3px 10px;border-radius:999px}
.reveal{opacity:0;translate:0 48px;transition:opacity .9s cubic-bezier(.22,1,.36,1),translate .9s cubic-bezier(.22,1,.36,1),transform .35s cubic-bezier(.22,1,.36,1),box-shadow .4s}.reveal.in{opacity:1;translate:0 0}
#lb{position:fixed;inset:0;background:#000d;display:none;align-items:center;justify-content:center;z-index:20;padding:16px;cursor:zoom-out}#lb.on{display:flex}#lb img{max-width:100%;max-height:100%;object-fit:contain;border-radius:12px}
footer{text-align:center;color:var(--mut);padding:26px;border-top:1px solid var(--bd);font-size:.9rem}
#top{position:fixed;right:16px;bottom:calc(16px + env(safe-area-inset-bottom,0px));width:44px;height:44px;border-radius:50%;border:1px solid var(--bd);background:#0a1438;color:#fff;font-size:1.2rem;cursor:pointer;display:none;z-index:6}

.orb{position:fixed;border-radius:50%;filter:blur(70px);opacity:.35;z-index:-1;animation:fl 14s ease-in-out infinite alternate}
.o1{width:300px;height:300px;background:#4d7bff;left:-90px;top:12%}.o2{width:260px;height:260px;background:#a855f7;right:-80px;top:55%;animation-delay:-6s}
@keyframes fl{to{transform:translate(40px,-60px) scale(1.2)}}
.mq{overflow:hidden;border-block:1px solid var(--bd);background:#0a1231aa;margin:8px -20px 10px;padding:12px 0;white-space:nowrap}
.mq div{display:inline-block;animation:mq 26s linear infinite;font-weight:700;color:#9bb4ff;letter-spacing:.04em}.mq span{margin:0 18px}.mq b{color:#c084fc}
@keyframes mq{to{transform:translateX(-50%)}}
.rail{margin:6px 0 4px;border:1px solid var(--bd);border-radius:18px;background:#0a1231aa;padding:16px 16px 12px}
.rail h4{margin:0 0 14px;font-size:.95rem;color:#b8c6ff}.rb{position:relative;height:10px;border-radius:99px;background:#121f52}
.rb i{position:absolute;top:0;height:100%;border-radius:99px;background:linear-gradient(90deg,var(--a),var(--b))}
.rb em{position:absolute;top:-5px;width:20px;height:20px;margin-left:-10px;border-radius:50%;background:#22d3a0;box-shadow:0 0 16px #22d3a0;transition:left 1s}
.rl{display:flex;justify-content:space-between;color:var(--mut);font-size:.75rem;margin-top:8px;font-family:ui-monospace,Menlo,monospace}
.card::after{content:"";position:absolute;inset:0;border-radius:22px;padding:1.5px;background:linear-gradient(120deg,transparent 30%,#6c8dff,#c084fc,transparent 70%);background-size:250%;-webkit-mask:linear-gradient(#000 0 0) content-box,linear-gradient(#000 0 0);-webkit-mask-composite:xor;mask-composite:exclude;opacity:0;transition:.4s;pointer-events:none;animation:sh 4s linear infinite}
.card:hover::after{opacity:1}@keyframes sh{to{background-position:-250%}}
.card.now::after{content:"NOW";inset:auto;right:12px;top:12px;padding:3px 10px;background:#22d3a0;opacity:1;-webkit-mask:none;mask:none;animation:none}
.quote{margin:20px 0;border:1px solid var(--bd);border-radius:22px;padding:28px 22px;text-align:center;background:linear-gradient(135deg,#102a7a55,#6b21a855);font-size:1.25rem;font-weight:700}
.quote small{display:block;margin-top:8px;color:var(--mut);font-weight:400;font-size:.9rem}
.tag{display:inline-block;margin-top:10px;font-size:.75rem;padding:3px 10px;border-radius:99px;background:#17338a;color:#c8d6ff}
#bar{transition:width .2s linear}
.mission{margin-top:10px}.mw{display:flex;gap:20px;align-items:center;flex-wrap:wrap;border:1px solid var(--bd);border-radius:22px;padding:20px;background:#0a1231aa;backdrop-filter:blur(6px)}
.rg{position:relative;width:120px;height:120px;flex:none}.rg svg{transform:rotate(-90deg)}.rg circle{fill:none;stroke-width:9}.rg .bg{stroke:#121f52}.rg #rg{stroke:url(#gr);stroke-linecap:round;stroke-dasharray:263.9;stroke-dashoffset:263.9;transition:stroke-dashoffset .9s cubic-bezier(.22,1,.36,1)}
.rg span{position:absolute;inset:0;display:grid;place-items:center;font-weight:800;font-size:1.3rem}
#ml{list-style:none;margin:0;padding:0;flex:1;min-width:220px}#ml li{display:flex;align-items:center;gap:12px;padding:11px 8px;border-radius:12px;cursor:pointer;transition:background .3s}#ml li:hover{background:#13236a55}#ml li b{flex:1;font-weight:600;transition:opacity .4s}#ml small{color:var(--mut);font-family:ui-monospace,Menlo,monospace}
.bx{width:22px;height:22px;border-radius:7px;border:2px solid #3555c0;transition:all .4s cubic-bezier(.22,1,.36,1);flex:none}
li.ck .bx{background:linear-gradient(135deg,var(--a),var(--b));border-color:transparent;box-shadow:0 0 14px #4d7bff88;transform:scale(1.1) rotate(8deg)}li.ck b{text-decoration:line-through;opacity:.5}
#ms{width:100%;text-align:center;color:var(--mut);margin:0}
@media(prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}.reveal{opacity:1;translate:0 0}}
.game{margin-top:10px}.gw{border:1px solid var(--bd);border-radius:22px;padding:14px;background:#0a1231aa;text-align:center;backdrop-filter:blur(6px)}
.gh{display:flex;justify-content:space-between;padding:0 6px 10px;font-weight:600;color:#b8c6ff}.gh b{color:#fff}
#gc{width:100%;max-width:420px;height:auto;border-radius:16px;border:1px solid var(--bd);touch-action:pan-y;display:block;margin:0 auto 12px;background:#050a1e}
.card,.btn,.chip{backface-visibility:hidden}.hero h1{will-change:translate}
.cm{margin-top:10px}.cbox{border:1px solid var(--bd);border-radius:22px;padding:16px;background:#0a1231aa;backdrop-filter:blur(6px)}
#ci{width:100%;resize:vertical;background:#050a1e;color:var(--tx);border:1px solid var(--bd);border-radius:14px;padding:12px;font:inherit;outline:none;transition:border-color .3s,box-shadow .3s}#ci:focus{border-color:var(--a);box-shadow:0 0 0 3px #4d7bff33}
.cr{display:flex;align-items:center;gap:10px;margin-top:10px;flex-wrap:wrap}.em{display:flex;gap:4px;flex:1}.em button{background:#0a1231;border:1px solid var(--bd);border-radius:10px;padding:5px 8px;font-size:1.1rem;cursor:pointer;transition:transform .3s cubic-bezier(.22,1,.36,1),background .3s}.em button.on{background:#17338a;border-color:var(--a);transform:scale(1.15)}
#cc{color:var(--mut);font-size:.8rem}#cs{margin:0;border:0;cursor:pointer;font:inherit;font-weight:600}#cs:disabled{opacity:.5;cursor:default}
.cnote{color:var(--mut);text-align:center;margin:12px 0}
#cl{margin-top:8px}.ci{position:relative;display:flex;gap:12px;padding:14px 4px;border-top:1px solid #16245a;animation:cin .5s cubic-bezier(.22,1,.36,1)}@keyframes cin{from{opacity:0;transform:translateY(10px)}}
.av{flex:none;width:38px;height:38px;border-radius:50%;display:grid;place-items:center;font-weight:800;background:linear-gradient(135deg,var(--a),var(--b))}
.cb{flex:1;min-width:0}.ch{display:flex;gap:8px;align-items:baseline;flex-wrap:wrap}.ch small{color:var(--mut)}.cb p{margin:2px 0 0;overflow-wrap:anywhere;color:#d3dbf7}
.cx{position:absolute;right:2px;top:10px;background:none;border:0;color:var(--mut);font-size:1.3rem;cursor:pointer}.cx:hover{color:#ff6b81}
#ld{position:fixed;inset:0;z-index:99;background:#030712;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:22px;transition:opacity .7s,visibility .7s}#ld.out{opacity:0;visibility:hidden}
.or{position:relative;width:120px;height:120px}.or i{position:absolute;inset:0;border-radius:50%;border:2px solid transparent;border-top-color:var(--a);animation:sp 1.2s linear infinite}.or i:nth-child(2){inset:14px;border-top-color:var(--b);animation-duration:1.8s;animation-direction:reverse}.or i:nth-child(3){inset:28px;border-top-color:#22d3a0;animation-duration:2.4s}
.or b{position:absolute;inset:44px;border-radius:50%;background:radial-gradient(var(--a),var(--b));box-shadow:0 0 30px var(--a);animation:pl 1.4s ease-in-out infinite}@keyframes sp{to{transform:rotate(360deg)}}@keyframes pl{50%{transform:scale(.6);opacity:.6}}
#ld .pc{font:700 1.4rem ui-monospace,Menlo,monospace;letter-spacing:.1em}#ld .ln{width:200px;height:3px;border-radius:9px;background:#0f1a45;overflow:hidden}#ld .ln em{display:block;height:100%;width:0;background:linear-gradient(90deg,var(--a),var(--b));transition:width .15s}#ld small{color:var(--mut)}
.fc{margin:50px 0 0;padding:26px;border:1px solid var(--bd);border-radius:22px;background:linear-gradient(180deg,#0c1840cc,#070d25cc);text-align:center}.fc h2{margin:0 0 4px}.fw{position:relative;width:200px;height:200px;margin:14px auto;transition:filter .4s}.fw svg{width:200px;height:200px;transform:rotate(-90deg)}.fw circle{fill:none;stroke-width:10;stroke-linecap:round}.fw .bg{stroke:#12205a}.fw .fg{stroke:url(#fgd);stroke-dasharray:553;stroke-dashoffset:0;transition:stroke-dashoffset 1s linear}
.fw b{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font:700 2.4rem ui-monospace,Menlo,monospace}.fc.run .fw{filter:drop-shadow(0 0 18px #4d7bff99)}.fr{display:flex;gap:8px;justify-content:center;flex-wrap:wrap;margin-top:10px}.fr .btn{border:0;cursor:pointer;font:inherit;font-weight:600;margin:0}#fm{min-height:1.6em;color:#22d3a0;font-weight:600;margin:12px 0 0}.fc small{color:var(--mut)}
.or{display:none}#ld{background:radial-gradient(ellipse at 50% 40%,#0b1640 0%,#030712 70%)}
.st{width:110px;height:110px;perspective:700px;transition:transform .8s cubic-bezier(.7,0,.3,1)}#ld.out .st{transform:scale(7)}
.fl{width:100%;height:100%;animation:fb 3s ease-in-out infinite}@keyframes fb{50%{transform:translateY(-16px)}}
.cu{position:relative;width:100%;height:100%;transform-style:preserve-3d;animation:cr 7s cubic-bezier(.65,0,.35,1) infinite}
@keyframes cr{0%{transform:rotateX(-25deg) rotateY(0) scale(1)}25%{transform:rotateX(-35deg) rotateY(90deg) scale(1.12)}50%{transform:rotateX(-15deg) rotateY(180deg) scale(1)}75%{transform:rotateX(-35deg) rotateY(270deg) scale(1.12)}100%{transform:rotateX(-25deg) rotateY(360deg) scale(1)}}
.cu span{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-size:2.9rem;border:1.5px solid #6c8dffaa;border-radius:14px;background:linear-gradient(135deg,#102060aa,#2a1160aa);box-shadow:inset 0 0 28px #4d7bff55,0 0 14px #4d7bff33}
.cu span:nth-child(1){transform:translateZ(55px)}.cu span:nth-child(2){transform:rotateY(90deg) translateZ(55px)}.cu span:nth-child(3){transform:rotateY(180deg) translateZ(55px)}.cu span:nth-child(4){transform:rotateY(-90deg) translateZ(55px)}.cu span:nth-child(5){transform:rotateX(90deg) translateZ(55px)}.cu span:nth-child(6){transform:rotateX(-90deg) translateZ(55px)}
.sh{width:96px;height:16px;margin-top:-6px;border-radius:50%;background:radial-gradient(#6c8dff88,transparent 70%);animation:sw 3s ease-in-out infinite}@keyframes sw{50%{transform:scale(.6);opacity:.5}}
.cu{animation:cr2 16s linear infinite;will-change:transform}@keyframes cr2{from{transform:rotateX(-24deg) rotateY(0)}to{transform:rotateX(-24deg) rotateY(360deg)}}
@keyframes fb{0%,100%{transform:translateY(0) rotateZ(-2deg)}50%{transform:translateY(-14px) rotateZ(2deg)}}.fl{animation-duration:5s;will-change:transform}.sh{animation-duration:5s}#ld .ln em{transition:none}
body{background:radial-gradient(ellipse at 18% 8%,#3a1580aa,transparent 55%),radial-gradient(ellipse at 88% 32%,#0e4a9a88,transparent 50%),radial-gradient(ellipse at 40% 100%,#7a1a6a66,transparent 55%),#01020a;background-attachment:fixed}
.pl{position:fixed;right:-90px;top:16vh;width:240px;height:240px;border-radius:50%;z-index:-1;pointer-events:none;background:radial-gradient(circle at 30% 28%,#a9c4ff,#4a5ce0 38%,#1a1068 70%,#080428);box-shadow:inset -34px -24px 60px #000d,0 0 70px #4d7bff55;animation:pd 26s ease-in-out infinite alternate}
.pl::before{content:'';position:absolute;left:-60px;right:-60px;top:50%;height:70px;margin-top:-35px;border:7px solid #d6b8ff66;border-radius:50%;transform:rotate(-20deg);box-shadow:0 0 18px #c084fc44}
.mn{position:fixed;left:6%;bottom:12vh;width:54px;height:54px;border-radius:50%;z-index:-1;pointer-events:none;background:radial-gradient(circle at 32% 30%,#f2f2ff,#8a8fb8 55%,#2a2d4a);box-shadow:inset -10px -8px 18px #000c,0 0 24px #aab4ff44;animation:pd 18s ease-in-out infinite alternate-reverse}
@keyframes pd{to{transform:translate(-30px,26px) rotate(8deg)}}
body{background:#000}.pl,.orb,.glow{display:none}
.mn{left:auto;bottom:auto;top:calc(11vh + env(safe-area-inset-top,0px));right:8vw;width:84px;height:84px;background:radial-gradient(circle at 60% 32%,#a9a697 0 8%,#0000 9%),radial-gradient(circle at 34% 62%,#a9a697 0 11%,#0000 12%),radial-gradient(circle at 70% 70%,#b3b0a2 0 6%,#0000 7%),radial-gradient(circle at 28% 30%,#fffef6 0%,#ebe8d8 35%,#bbb8a8 70%,#807d74 100%);box-shadow:inset -16px -12px 26px #000a,0 0 38px #fff4d055,0 0 90px #aab8ff33;animation:mf 9s ease-in-out infinite alternate}@keyframes mf{to{transform:translateY(10px)}}
.mn{overflow:hidden;pointer-events:auto;cursor:grab;touch-action:none;z-index:4;--sh:90px;user-select:none;-webkit-user-select:none}.mn.gr{cursor:grabbing}
#ld::before{content:'';position:absolute;inset:0;pointer-events:none;background-image:radial-gradient(1.5px 1.5px at 20px 30px,#fff,transparent),radial-gradient(1px 1px at 90px 120px,#cfe0ff,transparent),radial-gradient(1.5px 1.5px at 160px 60px,#ffd9b0,transparent),radial-gradient(1px 1px at 230px 200px,#fff,transparent),radial-gradient(2px 2px at 120px 250px,#b9a8ff,transparent);background-size:260px 260px;animation:dr 30s linear infinite;transition:transform 1s cubic-bezier(.7,0,.3,1)}#ld.out::before{transform:scale(2.6)}@keyframes dr{to{background-position:-260px 260px}}#ld>*{position:relative}
.btn,.chip.on,#top{background:radial-gradient(1px 1px at 14% 28%,#fff,transparent),radial-gradient(1.2px 1.2px at 72% 20%,#fff,transparent),radial-gradient(1px 1px at 38% 74%,#cfe0ff,transparent),radial-gradient(1.4px 1.4px at 88% 68%,#fff,transparent),radial-gradient(1px 1px at 55% 45%,#ffd9b0,transparent),radial-gradient(1px 1px at 24% 60%,#b9a8ff,transparent),linear-gradient(135deg,#05060e,#0b0d1c);border:1px solid #2b3160;box-shadow:0 0 18px #4d7bff22,inset 0 0 14px #00000088;color:#fff}.btn:hover,.chip.on:hover{border-color:#5a6ad0;box-shadow:0 0 26px #6c8dff44,inset 0 0 14px #00000088}
#ld::before{inset:-260px;will-change:transform;animation:dr2 30s linear infinite;transition:scale 1.1s cubic-bezier(.7,0,.3,1)}#ld.out::before{scale:2.6}@keyframes dr2{to{transform:translate(260px,260px)}}.st{will-change:transform}
.pb::before{width:200%;background-size:50% 100%;animation:ps2 6s linear infinite;will-change:transform}@keyframes ps2{to{transform:translateX(-50%)}}
#ld .ln em{width:100%;transform:scaleX(0);transform-origin:0 0;transition:none;will-change:transform}
#ld::before{inset:0;animation:tw 3.2s ease-in-out infinite alternate;will-change:opacity;transition:none}#ld.out::before{transform:none;scale:1}@keyframes tw{from{opacity:.5}to{opacity:1}}
#ld.out .st{transform:scale(1.5)}#ld.go .ln em{animation:bf 1.5s cubic-bezier(.25,.8,.25,1) forwards}@keyframes bf{to{transform:scaleX(1)}}
.tl{perspective:1400px}.card{border-radius:30px;margin-bottom:44px;background:linear-gradient(160deg,#101d52,#070d25);border-color:#2a3a86;box-shadow:inset 0 1px 0 #7f98ff55,0 7px 0 -1px #0b1340,0 13px 0 -3px #070b26,0 34px 46px -8px #000c}.card::after{border-radius:30px}
.card:hover{box-shadow:inset 0 1px 0 #7f98ff77,0 7px
