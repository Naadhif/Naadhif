<div align="center">

<!-- ░░ HACKER HEADER — Matrix Rain + Glitch ░░ -->
<img src="https://capsule-render.vercel.app/api?type=rect&color=000000&height=4&section=header" width="100%"/>

<table align="center" width="860" border="0" cellspacing="0" cellpadding="0">
<tr>
<td align="center">

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8"/>
<style>
*{margin:0;padding:0;box-sizing:border-box}
body{background:#000;width:860px;height:280px;overflow:hidden}
#cv{position:absolute;top:0;left:0;width:860px;height:280px;z-index:1}
.scan{position:absolute;top:0;left:0;width:100%;height:100%;z-index:3;pointer-events:none;
  background:repeating-linear-gradient(to bottom,transparent 0px,transparent 3px,rgba(0,0,0,0.15) 3px,rgba(0,0,0,0.15) 4px)}
.vign{position:absolute;top:0;left:0;width:100%;height:100%;z-index:4;pointer-events:none;
  background:radial-gradient(ellipse at 50% 50%,transparent 40%,rgba(0,0,0,0.75) 100%)}
.ui{position:absolute;inset:0;z-index:10;display:flex;flex-direction:column;justify-content:center;padding:0 48px;gap:8px}
/* Corner brackets */
.c{position:absolute;width:28px;height:28px;border-color:#00ff41;border-style:solid;z-index:12;
  box-shadow:0 0 6px #00ff41}
.tl{top:14px;left:14px;border-width:3px 0 0 3px}
.tr{top:14px;right:14px;border-width:3px 3px 0 0}
.bl{bottom:14px;left:14px;border-width:0 0 3px 3px}
.br{bottom:14px;right:14px;border-width:0 3px 3px 0}
/* Name */
.name-wrap{position:relative;display:inline-block}
.name{font-family:'Courier New',monospace;font-size:72px;font-weight:900;letter-spacing:18px;
  color:#00ff41;text-transform:uppercase;
  text-shadow:0 0 4px #00ff41,0 0 14px #00ff41,0 0 30px #00cc33,0 0 60px #009922;
  animation:flk 5s infinite;position:relative;z-index:2}
.name-g1,.name-g2{font-family:'Courier New',monospace;font-size:72px;font-weight:900;
  letter-spacing:18px;text-transform:uppercase;position:absolute;top:0;left:0;z-index:1}
.name-g1{color:#0ff;text-shadow:3px 0 #0ff;clip-path:polygon(0 0,100% 0,100% 40%,0 40%);
  animation:g1 3.5s infinite}
.name-g2{color:#f0f;text-shadow:-3px 0 #f0f;clip-path:polygon(0 60%,100% 60%,100% 100%,0 100%);
  animation:g2 3.5s infinite}
@keyframes g1{0%,86%,100%{transform:translate(0);opacity:0}88%{transform:translate(-6px,2px);opacity:.9}91%{transform:translate(6px,-2px);opacity:.9}93%{transform:translate(-3px,0);opacity:.7}95%{opacity:0}}
@keyframes g2{0%,79%,100%{transform:translate(0);opacity:0}81%{transform:translate(6px,-2px);opacity:.8}84%{transform:translate(-5px,3px);opacity:.8}86%{transform:translate(2px,0);opacity:.6}88%{opacity:0}}
@keyframes flk{0%,96%,100%{opacity:1}97%{opacity:.4}98%{opacity:1}99%{opacity:.7}}
/* Subtitle */
.sub{font-family:'Courier New',monospace;font-size:13px;letter-spacing:5px;color:#00cc33;
  text-transform:uppercase;text-shadow:0 0 8px #00ff41;opacity:.9;margin-top:2px}
/* Prompt */
.prompt{font-family:'Courier New',monospace;font-size:14px;color:#00ff41;letter-spacing:2px;
  text-shadow:0 0 8px #00ff41;margin-top:6px;display:flex;align-items:center;gap:4px}
.cur{display:inline-block;width:10px;height:16px;background:#00ff41;
  box-shadow:0 0 8px #00ff41;animation:bc 1s step-end infinite}
@keyframes bc{0%,100%{opacity:1}50%{opacity:0}}
</style>
</head>
<body>
<canvas id="cv"></canvas>
<div class="scan"></div>
<div class="vign"></div>
<div class="c tl"></div><div class="c tr"></div>
<div class="c bl"></div><div class="c br"></div>
<div class="ui">
  <div class="name-wrap">
    <div class="name-g1">NAADHIF</div>
    <div class="name-g2">NAADHIF</div>
    <div class="name">NAADHIF</div>
  </div>
  <div class="sub">Machine Learning &nbsp;|&nbsp; Information Retrieval &nbsp;|&nbsp; Data Science</div>
  <div class="prompt">root@github:~$ <span id="tp"></span><span class="cur"></span></div>
</div>

<script>
const cv=document.getElementById('cv');
const cx=cv.getContext('2d');
cv.width=860;cv.height=280;
const COLS=Math.floor(860/16);
const drops=Array.from({length:COLS},()=>Math.random()*-30|0);
const CHARS="01アイウエオカキクケコサシスセソNAADHIF{}[]<>;:|\\アヲンヴヅ";

function rain(){
  cx.fillStyle='rgba(0,0,0,0.055)';
  cx.fillRect(0,0,860,280);
  for(let i=0;i<COLS;i++){ ch="CHARS[Math.random()*CHARS.length|0];" const if(r r="Math.random();" y="drops[i]*16;">.96){cx.fillStyle='#ccffcc';cx.font='bold 13px monospace';}
    else if(r>.7){cx.fillStyle='#00ff41';cx.font='13px monospace';}
    else{cx.fillStyle='#004d14';cx.font='13px monospace';}
    cx.fillText(ch,i*16+2,y);
    if(y>280&&Math.random()>.974)drops[i]=0;
    drops[i]++;
  }
}
setInterval(rain,42);

// Typing
const lines=[
  "python  jupyter  nlp",
  "whoami  // Naadhif",
  "cat skills.txt",
  "ML | IR | DataScience",
  "git push origin main"
];
let li=0,ci=0,del=false;
const el=document.getElementById('tp');
function type(){
  if(!del){
    el.textContent=lines[li].slice(0,++ci);
    if(ci===lines[li].length){del=true;setTimeout(type,1600);return;}
  }else{
    el.textContent=lines[li].slice(0,--ci);
    if(ci===0){del=false;li=(li+1)%lines.length;}
  }
  setTimeout(type,del?35:80);
}
type();
</script>
</body>
</html>
