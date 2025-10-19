<!-- 💀 README: nappierbug — 17yo Code Enthusiast 💀 -->
<div align="center" style="background-color:black; color:#00FF00; padding:20px; font-family:'Courier New', monospace; border-radius:10px;">
<p align="center">
  <img src="https://komarev.com/ghpvc/?username=nappierbug&label=Profile%20Views&color=00ff00&style=for-the-badge" alt="Profile views counter" />
</p>
  <h1 style="color:#00FF00;">&lt; Initializing nappierbug... &gt;</h1>

  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&pause=1000&color=00FF00&center=true&vCenter=true&width=550&lines=%3E+Booting+Digital+Persona...;%3E+Access+Granted!;%3E+Welcome+to+nappierbug+HQ!;%3E+Stay+Curious..." alt="Typing SVG">

  <pre style="text-align:left; background-color:#000; color:#00FF00; padding:10px; border-radius:10px; border:1px solid #00FF00; width:80%; margin:auto;">
    ┌─────────────────────────────────────────────────────────────┐
    │  > PROFILE LOADED: nappierbug                              │
    ├─────────────────────────────────────────────────────────────┤
    │  AGE: 17                                                   │
    │  ROLE: Coder | Programmer | Security Enthusiast            │
    │  STATUS: Online & Learning...                              │
    │  MISSION: Transforming Code Into Magic ⚡                   │
    └─────────────────────────────────────────────────────────────┘
  </pre>

  <br>

  <h2 style="color:#00FF00;">About Me 🧠</h2>
  <p style="width:70%;margin:auto;color:#00FF00;">
    I’m <b>nappierbug</b>, a 17-year-old who loves <b>coding</b>, <b>programming</b>, and uncovering how systems work.  
    I live in the world of logic, algorithms, and digital exploration.  
    Always evolving, always learning — one line of code at a time. 👾
  </p>

  <br>
  <h2 style="color:#00FF00;">Connect with Me 📡</h2>
  <p>
    <a href="https://wa.me/254116141363" target="_blank">
      <img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
    </a>
    <a href="https://www.instagram.com/n.a.p.p.i.e.r?igsh=ZGUzMzM3NWJiOQ==" target="_blank">
      <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram">
    </a> 
    <!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>System Console — Secure Access</title>
<style>
  :root{--bg:#000;--green:#00ff66;--muted:#0b0b0b}
  html,body{height:100%;margin:0;background:var(--bg);color:var(--green);font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, "Roboto Mono", "Courier New", monospace}
  #wrap{position:relative;height:100%;overflow:hidden}
  canvas#matrix{position:absolute;inset:0;z-index:0;opacity:.55}
  .panel{position:relative;z-index:2;padding:24px;max-width:920px;margin:30px auto;background:linear-gradient(180deg, rgba(0,0,0,0.2), rgba(0,0,0,0.35));border:1px solid rgba(0,255,102,0.06);box-shadow:0 8px 30px rgba(0,0,0,0.6);border-radius:10px}
  h1{margin:0 0 6px;font-size:20px;color:var(--green);letter-spacing:1px}
  .controls{display:flex;gap:10px;margin:12px 0}
  button{background:#071; color:#000;border:0;padding:10px 14px;border-radius:6px;cursor:pointer;font-weight:700}
  button.secondary{background:transparent;color:var(--green);border:1px solid rgba(0,255,102,0.1)}
  .terminal{background:#000000aa;border-radius:6px;padding:18px;height:360px;overflow:auto;border:1px solid rgba(0,255,102,0.06)}
  .line{white-space:pre-wrap;line-height:1.4;color:var(--green);font-size:14px}
  .prompt{color:#9cffb1}
  .glow{ text-shadow: 0 0 6px rgba(0,255,102,0.15); }
  .progress{margin:8px 0;height:12px;background:#020202;border-radius:8px;overflow:hidden;border:1px solid rgba(0,255,102,0.08)}
  .bar{height:100%;width:0;background:linear-gradient(90deg,#00ff66,#00b36b)}
  .small{font-size:12px;color:#9aff9a;opacity:.85}
  footer{color:#77ff99;opacity:.55;margin-top:10px;font-size:12px;text-align:center}
  @keyframes blink {50%{opacity:0}}
  .cursor{display:inline-block;width:8px;height:16px;background:var(--green);margin-left:6px; animation: blink 1s steps(2) infinite;vertical-align:middle}
  /* typing label */
  .typing {display:inline-block;border-right:2px solid rgba(0,255,102,0.8);padding-right:6px}
</style>
</head>
<body>
<div id="wrap">
  <canvas id="matrix"></canvas>

  <div class="panel">
    <h1 class="glow">&lt; Secure Console v4.7 &gt;</h1>
    <div class="controls">
      <button id="startBtn">Start Prank</button>
      <button id="stopBtn" class="secondary">Stop</button>
      <div style="flex:1"></div>
      <div class="small">For fun only — harmless demo</div>
    </div>

    <div class="terminal" id="terminal" aria-live="polite">
      <div class="line prompt">> initializing secure connection...</div>
      <div class="line" id="out0"> </div>
      <div class="line" id="out1"></div>
      <div class="line" id="out2"></div>
      <div class="line" id="out3"></div>
      <div class="line" id="out4"></div>
      <div class="line" id="out5"></div>
      <div class="line" id="progressArea"></div>
    </div>

    <footer>Powered by MatrixSim • Press <strong>Stop</strong> to end</footer>
  </div>
</div>

<script>
/* ===== Matrix rain (canvas) ===== */
const canvas = document.getElementById('matrix');
const ctx = canvas.getContext('2d');
let w, h;
function resize(){ w = canvas.width = innerWidth; h = canvas.height = innerHeight; initCols(); }
window.addEventListener('resize', resize);
const fontSize = 16;
let cols = [];
function initCols(){
  cols = new Array(Math.floor(w / fontSize)).fill(0);
}
const chars = 'ᚠᛗᚱᚾ0123456789abcdef@#$%&*<>/|\\+-=';
resize();
function draw(){ 
  ctx.fillStyle = 'rgba(0,0,0,0.15)';
  ctx.fillRect(0,0,w,h);
  ctx.fillStyle = 'rgba(0,255,150,0.8)';
  ctx.font = fontSize + 'px monospace';
  for(let i=0;i<cols.length;i++){
    const x = i*fontSize;
    const char = chars.charAt(Math.floor(Math.random()*chars.length));
    ctx.fillText(char, x, cols[i]*fontSize);
    if(cols[i]*fontSize > h && Math.random() > 0.975) cols[i]=0;
    cols[i]++;
  }
  requestAnimationFrame(draw);
}
draw();

/* ===== Terminal typing + fake hack logic ===== */
const out = (...text) => {
  const t = document.createElement('div');
  t.className = 'line';
  t.textContent = text.join(' ');
  terminal.appendChild(t);
  terminal.scrollTop = terminal.scrollHeight;
};

const terminal = document.getElementById('terminal');
const startBtn = document.getElementById('startBtn');
const stopBtn = document.getElementById('stopBtn');

let seqTimer = null;
let audioCtx, oscillator, gainNode, running=false;

function beepSequence(){
  if(!audioCtx) {
    audioCtx = new (window.AudioContext || window.webkitAudioContext)();
    gainNode = audioCtx.createGain(); gainNode.gain.value = 0.05; gainNode.connect(audioCtx.destination);
  }
  // quick rhythmic beeps
  const now = audioCtx.currentTime;
  const freqs = [820, 640, 960, 520, 420];
  freqs.forEach((f,i)=>{
    const o = audioCtx.createOscillator();
    o.type = 'sine';
    o.frequency.value = f;
    o.connect(gainNode);
    o.start(now + i*0.09);
    o.stop(now + i*0.09 + 0.06);
  });
}

function lowDrone(duration=1.2){
  if(!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
  const o = audioCtx.createOscillator();
  const g = audioCtx.createGain();
  o.type='sawtooth';
  o.frequency.value = 120;
  g.gain.value = 0.02;
  o.connect(g); g.connect(audioCtx.destination);
  o.start();
  setTimeout(()=>{ g.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime+0.4); o.stop(); }, duration*1000);
}

/* Simulated sequences: typed lines, fake IPs, password tries, progress bars */
const seq = [
  {type:'type', text:'> opening secure socket...'},
  {type:'wait', ms:700},
  {type:'type', text:'> handshake: 0x4a3b... OK'},
  {type:'type', text:'> target: LAPTOP-USER-47.local (192.168.1.' + Math.floor(100+Math.random()*120)+')'},
  {type:'wait', ms:500},
  {type:'type', text:'> enumerating services: SSH, SMB, HTTP, RDP'},
  {type:'wait', ms:400},
  {type:'type', text:'> brute forcing default creds (this is fake)...'},
  {type:'progress', label:'CRACKING-CREDENTIALS', time: 3500},
  {type:'beep'},
  {type:'type', text:'> credentials found: user:friend ; pass: ********'},
  {type:'type', text:'> dumping "secrets" (fake)...'},
  {type:'progress', label:'DUMPING-DATA', time: 2200},
  {type:'beepSequence'},
  {type:'type', text:'> exploit complete. remote shell simulated.'},
  {type:'wait', ms:350},
  {type:'type', text:'> echo "you have been pranked 😉"'},
  {type:'final'}
];

function runSeq(){
  let i=0;
  running=true;
  function next(){
    if(!running) return;
    const step = seq[i++];
    if(!step){ running=false; return; }
    if(step.type==='type'){
      typeLine(step.text, ()=> setTimeout(next, 220));
    } else if(step.type==='wait'){
      setTimeout(next, step.ms);
    } else if(step.type==='progress'){
      runProgress(step.label, step.time, next);
    } else if(step.type==='beep'){
      lowDrone(0.8); setTimeout(next, 200);
    } else if(step.type==='beepSequence'){
      beepSequence(); setTimeout(next, 300);
    } else if(step.type==='final'){
      typeLine('> [SIMULATION COMPLETE] — friendly prank mode.', ()=>{ running=false; });
    }
  }
  next();
}

function typeLine(text, cb){
  const line = document.createElement('div');
  line.className='line';
  terminal.appendChild(line);
  let pos=0;
  const speed = 18 + Math.random()*30;
  const anim = setInterval(()=>{
    line.textContent = text.slice(0,pos+1);
    terminal.scrollTop = terminal.scrollHeight;
    pos++;
    if(pos >= text.length){
      clearInterval(anim);
      cb && cb();
    }
  }, speed);
}

function runProgress(label, timeMs, cb){
  const wrapper = document.createElement('div');
  wrapper.className='line';
  wrapper.innerHTML = `${label} <span class="small">[working]</span>`;
  const progress = document.createElement('div');
  progress.className='progress';
  const bar = document.createElement('div');
  bar.className='bar';
  progress.appendChild(bar);
  wrapper.appendChild(progress);
  terminal.appendChild(wrapper);
  terminal.scrollTop = terminal.scrollHeight;

  const start = Date.now();
  const end = start + timeMs;
  const step = setInterval(()=>{
    const now = Date.now();
    const pct = Math.min(1, (now-start)/(end-start));
    bar.style.width = (pct*100)+'%';
    if(pct>=1){ clearInterval(step); cb && cb(); }
  }, 60);
}

/* Buttons */
startBtn.addEventListener('click', ()=>{
  if(running) return;
  // allow audio on user gesture
  if(!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
  lowDrone(0.6);
  seq.forEach(el=>{}); // noop
  // clear terminal area
  Array.from(terminal.querySelectorAll('.line')).forEach((n,i)=>{ if(i>0) n.remove(); }); // keep first prompt
  runSeq();
});
stopBtn.addEventListener('click', ()=>{
  running=false;
  const t = document.createElement('div');
  t.className='line';
  t.textContent='> simulation stopped by user.';
  terminal.appendChild(t);
  terminal.scrollTop = terminal.scrollHeight;
});

/* small safety: pressing Esc stops */
window.addEventListener('keydown', e=>{
  if(e.key==='Escape'){ running=false; const t=document.createElement('div');t.className='line';t.textContent='> [ESC] simulation aborted.'; terminal.appendChild(t); terminal.scrollTop=terminal.scrollHeight; }
});
</script>
</body>
</html>
