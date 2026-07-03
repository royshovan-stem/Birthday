<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday, Progga</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,600;1,500&family=Marcellus&family=Work+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink-green:#0B3D2E;
    --deep-green:#082A20;
    --gold:#D4AF37;
    --gold-soft:#E9CE7A;
    --cream:#FBF5E6;
    --ember:#C1440E;
    --blush:#F3D9C4;
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    background:
      radial-gradient(ellipse at 20% -10%, rgba(212,175,55,0.15), transparent 55%),
      radial-gradient(ellipse at 85% 110%, rgba(193,68,14,0.18), transparent 50%),
      linear-gradient(180deg, var(--deep-green), var(--ink-green) 45%, #0a3327 100%);
    color:var(--cream);
    font-family:'Work Sans', sans-serif;
    min-height:100vh;
    overflow-x:hidden;
    position:relative;
  }
  /* floating gold motes */
  .motes{position:fixed; inset:0; pointer-events:none; z-index:1;}
  .mote{position:absolute; border-radius:50%; background:var(--gold-soft); opacity:0.5; filter:blur(0.5px); animation:float linear infinite;}
  @keyframes float{
    0%{transform:translateY(0) translateX(0); opacity:0;}
    10%{opacity:0.6;}
    90%{opacity:0.5;}
    100%{transform:translateY(-110vh) translateX(20px); opacity:0;}
  }

  .wrap{position:relative; z-index:2; max-width:880px; margin:0 auto; padding:0 24px;}

  /* HERO */
  .hero{
    min-height:100svh;
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:60px 24px;
  }
  .eyebrow{
    font-family:'Marcellus', serif;
    letter-spacing:0.45em;
    text-transform:uppercase;
    font-size:12px;
    color:var(--gold-soft);
    opacity:0;
    animation:riseIn 1s ease forwards 0.2s;
  }
  .eyebrow::before,.eyebrow::after{content:'✦'; margin:0 14px; color:var(--gold); font-size:10px; vertical-align:middle;}

  .hero h1{
    font-family:'Cormorant Garamond', serif;
    font-weight:600;
    font-size:clamp(2.6rem, 9vw, 6.2rem);
    line-height:1.02;
    margin-top:22px;
    background:linear-gradient(180deg, #fff6df 0%, var(--gold-soft) 55%, var(--gold) 100%);
    -webkit-background-clip:text;
    background-clip:text;
    color:transparent;
    opacity:0;
    animation:riseIn 1.1s ease forwards 0.5s;
    text-shadow:0 0 60px rgba(212,175,55,0.25);
  }
  .hero .name{
    font-family:'Cormorant Garamond', serif;
    font-style:italic;
    font-weight:500;
    font-size:clamp(2.2rem, 7.5vw, 4.6rem);
    margin-top:6px;
    color:var(--cream);
    opacity:0;
    animation:riseIn 1.1s ease forwards 0.85s;
    letter-spacing:0.01em;
  }
  .hero .subname{
    display:block;
    font-family:'Work Sans', sans-serif;
    font-size:clamp(0.75rem, 2vw, 0.95rem);
    letter-spacing:0.2em;
    text-transform:uppercase;
    color:var(--blush);
    opacity:0;
    animation:riseIn 1s ease forwards 1.15s;
    margin-top:18px;
  }

  @keyframes riseIn{
    from{opacity:0; transform:translateY(18px);}
    to{opacity:1; transform:translateY(0);}
  }

  .scroll-cue{
    margin-top:64px;
    opacity:0;
    animation:riseIn 1s ease forwards 1.6s, bob 2.4s ease-in-out infinite 2.6s;
    font-size:11px;
    letter-spacing:0.3em;
    text-transform:uppercase;
    color:rgba(251,245,230,0.55);
  }
  @keyframes bob{
    0%,100%{transform:translateY(0);}
    50%{transform:translateY(8px);}
  }

  /* DIVIDER */
  .divider{
    display:flex; align-items:center; justify-content:center; gap:16px;
    margin:0 auto 70px; max-width:280px;
  }
  .divider .line{flex:1; height:1px; background:linear-gradient(90deg, transparent, rgba(212,175,55,0.5), transparent);}
  .divider .mark{color:var(--gold); font-size:14px;}

  /* MESSAGE SECTION */
  .message-section{
    padding:40px 24px 120px;
    text-align:center;
  }
  .message-card{
    max-width:640px;
    margin:0 auto;
    padding:56px 40px;
    border:1px solid rgba(212,175,55,0.3);
    border-radius:2px;
    background:linear-gradient(180deg, rgba(212,175,55,0.06), rgba(212,175,55,0.02));
    position:relative;
  }
  .message-card::before,.message-card::after{
    content:'';
    position:absolute;
    width:22px; height:22px;
    border:1px solid var(--gold);
    opacity:0.7;
  }
  .message-card::before{top:-1px; left:-1px; border-right:none; border-bottom:none;}
  .message-card::after{bottom:-1px; right:-1px; border-left:none; border-top:none;}

  .message-eyebrow{
    font-family:'Marcellus', serif;
    font-size:11px;
    letter-spacing:0.35em;
    text-transform:uppercase;
    color:var(--gold-soft);
    margin-bottom:26px;
  }
  .message-card p.line1{
    font-family:'Cormorant Garamond', serif;
    font-size:clamp(1.6rem, 4vw, 2.35rem);
    line-height:1.5;
    color:var(--cream);
    font-weight:500;
  }
  .message-card p.line1 em{
    font-style:italic;
    color:var(--gold-soft);
  }
  .message-card .signoff{
    margin-top:34px;
    font-size:13px;
    letter-spacing:0.15em;
    text-transform:uppercase;
    color:rgba(251,245,230,0.6);
  }

  /* CANDLE / WISH SECTION - signature element */
  .wish-section{
    padding:0 24px 140px;
    text-align:center;
    display:flex;
    flex-direction:column;
    align-items:center;
  }
  .wish-heading{
    font-family:'Cormorant Garamond', serif;
    font-style:italic;
    font-size:clamp(1.4rem,3.5vw,1.9rem);
    color:var(--blush);
    margin-bottom:48px;
    max-width:520px;
  }

  .cake{
    position:relative;
    width:220px;
    cursor:pointer;
    user-select:none;
    -webkit-tap-highlight-color:transparent;
  }
  .candle{
    position:relative;
    width:8px;
    height:46px;
    margin:0 auto;
    background:linear-gradient(180deg, var(--blush), var(--gold-soft));
    border-radius:3px;
  }
  .flame{
    position:absolute;
    top:-26px; left:50%;
    transform:translateX(-50%);
    width:14px; height:24px;
    background:radial-gradient(circle at 50% 70%, #fff6d8, var(--gold) 55%, var(--ember) 100%);
    border-radius:50% 50% 50% 50% / 60% 60% 40% 40%;
    filter:drop-shadow(0 0 10px rgba(212,175,55,0.9)) drop-shadow(0 0 22px rgba(193,68,14,0.6));
    animation:flicker 1.6s ease-in-out infinite;
    transform-origin:bottom center;
    transition:opacity 0.5s ease, transform 0.5s ease;
  }
  @keyframes flicker{
    0%,100%{transform:translateX(-50%) rotate(-3deg) scaleY(1);}
    50%{transform:translateX(-50%) rotate(3deg) scaleY(1.08);}
  }
  .flame.out{
    opacity:0;
    transform:translateX(-50%) translateY(-14px) scaleY(0.3);
  }
  .smoke{
    position:absolute;
    top:-30px; left:50%;
    width:3px; height:3px;
    background:rgba(255,255,255,0.5);
    border-radius:50%;
    opacity:0;
    filter:blur(2px);
  }
  .smoke.rise{animation:smokeRise 1.8s ease-out forwards;}
  @keyframes smokeRise{
    0%{opacity:0.6; transform:translate(-50%,0) scale(1);}
    100%{opacity:0; transform:translate(-30%,-70px) scale(6);}
  }
  .tier{
    margin-top:8px;
    border-radius:6px 6px 3px 3px;
    background:linear-gradient(180deg, var(--ember), #8f3009);
    box-shadow:inset 0 -8px 14px rgba(0,0,0,0.25), 0 10px 24px rgba(0,0,0,0.35);
  }
  .tier.top{width:120px; height:38px; margin-left:50px;}
  .tier.bottom{width:200px; height:52px; margin-left:10px; background:linear-gradient(180deg, var(--gold), #a97e18);}
  .drip{
    position:absolute; top:-2px; width:100%; height:12px;
    background-image:radial-gradient(circle, var(--cream) 40%, transparent 42%);
    background-size:20px 20px;
    background-position:0 -6px;
    opacity:0.9;
  }

  .cake-caption{
    margin-top:26px;
    font-size:12px;
    letter-spacing:0.25em;
    text-transform:uppercase;
    color:rgba(251,245,230,0.55);
    transition:opacity 0.4s ease;
  }

  .wish-reveal{
    max-width:520px;
    margin-top:36px;
    opacity:0;
    max-height:0;
    overflow:hidden;
    transition:opacity 0.9s ease, max-height 0.9s ease, margin-top 0.9s ease;
  }
  .wish-reveal.show{
    opacity:1;
    max-height:300px;
    margin-top:36px;
  }
  .wish-reveal p{
    font-family:'Cormorant Garamond', serif;
    font-size:clamp(1.2rem,3vw,1.5rem);
    line-height:1.7;
    color:var(--gold-soft);
  }

  footer{
    text-align:center;
    padding:40px 24px 60px;
    font-size:11px;
    letter-spacing:0.2em;
    text-transform:uppercase;
    color:rgba(251,245,230,0.35);
  }

  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.01ms !important; animation-iteration-count:1 !important; transition-duration:0.01ms !important;}
  }

  button, .cake{
    outline-offset:4px;
  }
  .cake:focus-visible{
    outline:2px solid var(--gold-soft);
  }
</style>
</head>
<body>

<div class="motes" id="motes"></div>

<div class="wrap">
  <section class="hero">
    <div class="eyebrow">A day of celebration</div>
    <h1>Happy Birthday</h1>
    <span class="name">Shariful Islam Khan <em>Progga</em></span>
    <span class="subname">Wishing you a year as bright as this day</span>
    <div class="scroll-cue">scroll down ↓</div>
  </section>

  <div class="divider"><span class="line"></span><span class="mark">✦</span><span class="line"></span></div>

  <section class="message-section">
    <div class="message-card">
      <div class="message-eyebrow">A wish for you</div>
      <p class="line1">May God bless you and <em>fulfil all of your good wishes.</em></p>
      <div class="signoff">— with warmth, on your special day</div>
    </div>
  </section>

  <section class="wish-section">
    <p class="wish-heading">Make a wish, Progga. Tap the flame when you're ready.</p>
    <div class="cake" id="cake" role="button" tabindex="0" aria-label="Blow out the candle to reveal a wish">
      <div class="candle">
        <div class="flame" id="flame"></div>
        <div class="smoke" id="smoke"></div>
      </div>
      <div class="tier top"><div class="drip"></div></div>
      <div class="tier bottom"><div class="drip"></div></div>
    </div>
    <div class="cake-caption" id="caption">tap the candle</div>
    <div class="wish-reveal" id="wishReveal">
      <p>Every wish you made just now — may it find its way to you. Happy Birthday, Progga. 🤍</p>
    </div>
  </section>

  <footer>Made with care, for Progga's birthday</footer>
</div>

<script>
  // ambient floating motes
  const motesContainer = document.getElementById('motes');
  const MOTE_COUNT = 26;
  for(let i=0;i<MOTE_COUNT;i++){
    const m = document.createElement('div');
    m.className = 'mote';
    const size = 2 + Math.random()*4;
    m.style.width = size+'px';
    m.style.height = size+'px';
    m.style.left = Math.random()*100+'%';
    m.style.bottom = -(Math.random()*20)+'px';
    m.style.animationDuration = (8 + Math.random()*10)+'s';
    m.style.animationDelay = (Math.random()*10)+'s';
    motesContainer.appendChild(m);
  }

  // candle blow interaction
  const cake = document.getElementById('cake');
  const flame = document.getElementById('flame');
  const smoke = document.getElementById('smoke');
  const caption = document.getElementById('caption');
  const wishReveal = document.getElementById('wishReveal');
  let blown = false;

  function blowCandle(){
    if(blown) return;
    blown = true;
    flame.classList.add('out');
    smoke.classList.add('rise');
    caption.textContent = 'wish made ✦';
    setTimeout(()=>{ wishReveal.classList.add('show'); }, 500);
  }

  cake.addEventListener('click', blowCandle);
  cake.addEventListener('keydown', (e)=>{
    if(e.key === 'Enter' || e.key === ' '){
      e.preventDefault();
      blowCandle();
    }
  });
</script>

</body>
</html>
