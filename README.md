
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#ffb6d5">
<title>Elizabeth's Pink Paradise 💗</title>

<style>
*{box-sizing:border-box}
body{
 margin:0;
 font-family:Georgia,serif;
 color:#87365f;
 background:linear-gradient(140deg,#fff0f7,#f7c9e1,#e9d4ff);
 min-height:100vh;
 overflow-x:hidden;
}
button{font-family:inherit;cursor:pointer}
.app{
 max-width:480px;
 min-height:100vh;
 margin:auto;
 padding:20px 16px 35px;
 text-align:center;
 position:relative;
 overflow:hidden;
}
.topline{
 letter-spacing:4px;
 font:11px Arial,sans-serif;
 color:#b65b88;
 margin:12px 0 24px;
}
.brand{
 font-size:19px;
 letter-spacing:2px;
 color:#a64276;
}
.screen{
 display:none;
 min-height:75vh;
 flex-direction:column;
 align-items:center;
 justify-content:center;
 animation:appear .8s ease;
}
.screen.active{display:flex}
@keyframes appear{
 from{opacity:0;transform:translateY(22px)}
 to{opacity:1;transform:translateY(0)}
}
h1{
 font-size:clamp(32px,9vw,46px);
 line-height:1.15;
 color:#b43f7e;
 margin:18px 0;
 text-shadow:0 3px 15px #fff;
}
h2{color:#b34b80}
p{font-size:17px;line-height:1.8}
.small{font:11px Arial,sans-serif;letter-spacing:3px}
.hero-art{
 width:230px;height:230px;
 border-radius:50%;
 display:grid;place-items:center;
 background:radial-gradient(circle,#fff 5%,#ffe2f0 48%,#eeb5d2 75%,#d98ab9);
 box-shadow:0 0 35px #d77cab88, inset 0 0 20px white;
 position:relative;
 animation:float 4s ease-in-out infinite;
}
.hero-art span{font-size:105px;filter:drop-shadow(0 8px 8px #a54b8055)}
@keyframes float{
 50%{transform:translateY(-13px) rotate(3deg)}
}
.butterfly{
 position:absolute;
 font-size:38px;
 animation:fly 5s ease-in-out infinite;
}
.b1{top:8%;left:5%}
.b2{right:5%;top:20%;animation-delay:1s}
.b3{bottom:12%;left:12%;animation-delay:2s}
@keyframes fly{
 0%,100%{transform:translate(0,0) rotate(-10deg)}
 50%{transform:translate(15px,-22px) rotate(15deg)}
}
.btn{
 border:0;
 padding:15px 26px;
 border-radius:40px;
 margin:10px;
 color:white;
 font-size:16px;
 background:linear-gradient(110deg,#f18bbd,#bb5a98);
 box-shadow:0 7px 18px #bc639455;
}
.btn:active{transform:scale(.96)}
.btn.light{
 background:#fff;
 color:#b34b80;
 border:1px solid #f1bdd8;
}
.glass{
 width:100%;
 padding:25px 20px;
 border:1px solid #fff;
 border-radius:25px;
 background:#ffffffa8;
 box-shadow:0 12px 35px #a64b7830;
 backdrop-filter:blur(8px);
}
.ribbon{
 display:inline-block;
 padding:8px 18px;
 border-radius:30px;
 background:#ffe0ee;
 color:#a64276;
 letter-spacing:2px;
 font:11px Arial,sans-serif;
}
.letter{
 font-size:17px;
 line-height:2;
 text-align:center;
}
.doll{
 font-size:90px;
 filter:drop-shadow(0 9px 8px #a94d7855);
 animation:float 3s infinite;
}
.gallery{
 display:grid;
 grid-template-columns:1fr 1fr;
 gap:12px;
 width:100%;
 margin:18px 0;
}
.photo{
 min-height:145px;
 border:2px solid white;
 border-radius:18px;
 background:linear-gradient(140deg,#ffe0ed,#ead5ff);
 display:grid;
 place-items:center;
 overflow:hidden;
 box-shadow:0 5px 16px #9b477a22;
}
.photo img{width:100%;height:150px;object-fit:cover}
.photo span{font-size:35px}
input{display:none}
.upload{
 display:inline-block;
 background:white;
 border:1px dashed #d879a8;
 border-radius:25px;
 padding:13px 20px;
 color:#a64276;
 cursor:pointer;
}
.timeline{
 text-align:left;
 border-left:2px solid #e99ac0;
 padding-left:18px;
 margin:15px 0;
}
.memory{
 background:#fff7fb;
 padding:13px;
 border-radius:14px;
 margin:12px 0;
}
.footer{
 font:11px Arial,sans-serif;
 letter-spacing:2px;
 margin:30px 0 10px;
 color:#a85c83;
}
.heart{
 position:fixed;
 bottom:-30px;
 pointer-events:none;
 animation:rise 7s linear forwards;
 z-index:5;
}
@keyframes rise{
 to{transform:translateY(-110vh) rotate(360deg);opacity:0}
}
.sparkle{
 position:fixed;
 pointer-events:none;
 color:white;
 animation:twinkle 2s infinite alternate;
}
@keyframes twinkle{to{opacity:.2;transform:scale(.5)}}
</style>
</head>

<body>
<main class="app">

<div class="topline">✧ A LITTLE WORLD MADE FOR YOU ✧</div>
<div class="brand">ELIZABETH'S PINK PARADISE ♡</div>

<span class="butterfly b1">🦋</span>
<span class="butterfly b2">🦋</span>
<span class="butterfly b3">🦋</span>

<!-- WELCOME -->
<section class="screen active" id="welcome">
 <div class="ribbon">A SPECIAL SURPRISE</div>
 <div class="hero-art">
  <span>🦋</span>
 </div>
 <h1>Welcome to Your<br>Pink Paradise</h1>
 <p>A magical little world created just for you, Elizabeth. 💗</p>
 <button class="btn" onclick="show('birthday')">Open Your Surprise ✨</button>
</section>

<!-- BIRTHDAY -->
<section class="screen" id="birthday">
 <div class="doll">👑</div>
 <div class="ribbon">TODAY IS YOUR DAY</div>
 <h1>Happy Birthday,<br>Elizabeth!</h1>
 <p>To the girl who makes the world more beautiful just by being in it.</p>
 <button class="btn" onclick="show('letter')">Read Your Letter 💌</button>
</section>

<!-- LETTER -->
<section class="screen" id="letter">
 <div class="doll">💌</div>
 <h1>A Little Love Note</h1>
 <div class="glass letter">
  My dearest Elizabeth,<br><br>
  You make my ordinary days special. Your smile is my favourite thing, and I'm lucky to have you in my life.<br><br>
  Every little moment with you is a memory I want to keep forever.<br><br>
  Hey, stop being too cute, the app might freeze! 😂<br><br>
  <strong>With lots of love, always. 💗</strong>
 </div>
 <button class="btn" onclick="show('memories')">Our Beautiful Story 🌷</button>
</section>

<!-- MEMORIES -->
<section class="screen" id="memories">
 <div class="doll">🎀</div>
 <h1>Our Beautiful Story</h1>
 <p>Every memory has a little piece of my heart.</p>
 <div class="glass">
  <div class="timeline">
   <div class="memory">🌸 <strong>Our Beginning</strong><br>Where our special story began.</div>
   <div class="memory">💕 <strong>Beautiful Moments</strong><br>All the smiles and memories we share.</div>
   <div class="memory">🦋 <strong>More Adventures</strong><br>Here's to many more moments together.</div>
  </div>
 </div>
 <button class="btn" onclick="show('gallery')">See Our Photos 📸</button>
</section>

<!-- GALLERY -->
<section class="screen" id="gallery">
 <div class="doll">📸</div>
 <h1>Our Memories</h1>
 <p>Add your favourite pictures here, beautiful.</p>
 <label class="upload" for="photos">＋ Add Your Photos</label>
 <input id="photos" type="file" accept="image/*" multiple>
 <div class="gallery" id="galleryGrid">
  <div class="photo"><span>💗</span></div>
  <div class="photo"><span>🌷</span></div>
  <div class="photo"><span>🦋</span></div>
  <div class="photo"><span>🎀</span></div>
 </div>
 <button class="btn" onclick="show('final')">One Last Surprise 💖</button>
</section>

<!-- FINAL -->
<section class="screen" id="final">
 <div class="hero-art"><span>👑</span></div>
 <h1>Forever My<br>Favourite Person</h1>
 <div class="glass">
  <p>Happy Birthday once again, Elizabeth! 💗</p>
  <p>May your life always be filled with happiness, love, magic and beautiful dreams.</p>
  <h2>Keep Smiling, Beautiful! 🦋</h2>
 </div>
 <button class="btn light" onclick="show('welcome')">Replay Our Story ↻</button>
</section>

<div class="footer">MADE WITH LOVE FOR ELIZABETH ♡</div>
</main>

<script>
function show(id){
 document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active'));
 document.getElementById(id).classList.add('active');
 window.scrollTo({top:0,behavior:'smooth'});
}

document.getElementById('photos').addEventListener('change',function(){
 const grid=document.getElementById('galleryGrid');
 for(const file of this.files){
  if(!file.type.startsWith('image/'))continue;
  const reader=new FileReader();
  reader.onload=function(e){
   const card=document.createElement('div');
   card.className='photo';
   const img=document.createElement('img');
   img.src=e.target.result;
   img.alt='Our memory';
   card.appendChild(img);
   grid.appendChild(card);
  };
  reader.readAsDataURL(file);
 }
});

function floatingHeart(){
 const heart=document.createElement('div');
 heart.className='heart';
 heart.textContent=['💗','💕','✨','🦋','🎀'][Math.floor(Math.random()*5)];
 heart.style.left=Math.random()*100+'vw';
 heart.style.fontSize=(16+Math.random()*20)+'px';
 document.body.appendChild(heart);
 setTimeout(()=>heart.remove(),7000);
}
setInterval(floatingHeart,1100);

for(let i=0;i<12;i++){
 const star=document.createElement('div');
 star.className='sparkle';
 star.textContent='✧';
 star.style.left=Math.random()*100+'vw';
 star.style.top=Math.random()*100+'vh';
 star.style.animationDelay=Math.random()*2+'s';
 document.body.appendChild(star);
}
</script>
</body>
</html>

<!-- LIZZY'S LIVE BIRTHDAY COUNTDOWN -->
<section id="birthday-countdown">
  <h2>🎂 Counting Down to Your Special Day 💗</h2>
  <p class="countdown-message">
    Every second brings us closer to celebrating you, my beautiful Lizzy! 🦋
  </p>

  <div class="countdown-boxes">
    <div><span id="days">0</span><small>Days</small></div>
    <div><span id="hours">0</span><small>Hours</small></div>
    <div><span id="minutes">0</span><small>Minutes</small></div>
    <div><span id="seconds">0</span><small>Seconds</small></div>
  </div>

  <p id="birthday-message">
    You deserve all the happiness in the world! 💕
  </p>
</section>

<style>
#birthday-countdown {
  margin: 35px 12px;
  padding: 30px 15px;
  text-align: center;
  border-radius: 25px;
  background: linear-gradient(135deg, #ffb6d9, #e8c5ff);
  color: #7c2455;
  box-shadow: 0 8px 25px #d98ab855;
}
#birthday-countdown h2 {
  font-size: 25px;
}
.countdown-message {
  font-size: 15px;
  line-height: 1.6;
}
.countdown-boxes {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 8px;
  margin: 25px 0;
}
.countdown-boxes div {
  background: #ffffffdd;
  padding: 15px 4px;
  border-radius: 15px;
}
.countdown-boxes span {
  display: block;
  font-size: 27px;
  font-weight: bold;
}
.countdown-boxes small {
  font-size: 12px;
}
#birthday-message {
  font-weight: bold;
}
</style>

<script>
function updateBirthdayCountdown() {
  const now = new Date();

  let year = now.getFullYear();
  let birthday = new Date(year, 11, 9, 0, 0, 0);

  if (now >= birthday) {
    birthday = new Date(year + 1, 11, 9, 0, 0, 0);
  }

  const difference = birthday - now;

  const days = Math.floor(difference / 86400000);
  const hours = Math.floor((difference % 86400000) / 3600000);
  const minutes = Math.floor((difference % 3600000) / 60000);
  const seconds = Math.floor((difference % 60000) / 1000);

  document.getElementById("days").textContent = days;
  document.getElementById("hours").textContent = hours;
  document.getElementById("minutes").textContent = minutes;
  document.getElementById("seconds").textContent = seconds;
}

updateBirthdayCountdown();
setInterval(updateBirthdayCountdown, 1000);
</script>

