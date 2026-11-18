
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elizabeth's Pink Paradise 💗</title>

<style>
*{box-sizing:border-box}
body{
 margin:0;
 font-family:Georgia,serif;
 color:#71345f;
 background:linear-gradient(135deg,#ffe4f2,#e8d5ff,#fff0f8);
 text-align:center;
 overflow-x:hidden;
}
section{
 min-height:100vh;
 display:flex;
 align-items:center;
 justify-content:center;
 padding:30px 16px;
}
.card{
 max-width:760px;
 width:100%;
 padding:35px 22px;
 border-radius:28px;
 background:#ffffffdf;
 border:2px solid white;
 box-shadow:0 12px 45px #b66caa55;
}
h1{font-size:clamp(36px,8vw,65px);color:#d84d9e}
h2{font-size:clamp(27px,6vw,42px);color:#bd4c98}
p{font-size:17px;line-height:1.8}
.script{font-style:italic;color:#a14c8c;font-size:22px}
button{
 border:0;border-radius:30px;padding:14px 25px;
 background:linear-gradient(120deg,#ec75b9,#a77be8);
 color:white;font-size:16px;cursor:pointer;
 margin:10px;box-shadow:0 5px 15px #c77dbb66;
}
button:hover{transform:scale(1.04)}
input[type="password"]{
 width:min(100%,280px);
 padding:15px;
 border:2px solid #e8b4d5;
 border-radius:25px;
 text-align:center;
 font-size:20px;
 letter-spacing:5px;
 outline:none;
}
.hidden{display:none!important}
.butterfly{
 position:fixed;z-index:3;pointer-events:none;
 font-size:30px;animation:fly 9s ease-in-out infinite;
}
.b1{top:12%;left:8%}
.b2{top:35%;right:8%;animation-delay:2s}
.b3{bottom:12%;left:15%;animation-delay:4s}
@keyframes fly{
 0%,100%{transform:translateY(0) rotate(-12deg)}
 50%{transform:translateY(-35px) rotate(15deg)}
}
.sparkle{
 position:fixed;pointer-events:none;
 animation:rise 9s linear infinite;
}
@keyframes rise{
 from{transform:translateY(100vh);opacity:0}
 20%{opacity:1}
 to{transform:translateY(-100vh);opacity:0}
}
.cake{font-size:85px;animation:bounce 2s infinite}
@keyframes bounce{50%{transform:translateY(-12px)}}
.countdown{
 display:grid;grid-template-columns:repeat(4,1fr);
 gap:9px;margin:25px 0;
}
.time{
 background:#fff0f8;padding:17px 4px;
 border-radius:16px;border:1px solid #f1c3df;
}
.time strong{
 display:block;font:bold 30px Arial;color:#d34c9b
}
.time span{font:11px Arial;text-transform:uppercase}
.letter{
 background:#fff8fc;padding:22px;border-radius:18px;
 text-align:left;line-height:1.9;border-left:4px solid #e38abd;
}
.gallery{
 display:grid;grid-template-columns:repeat(2,1fr);
 gap:12px;margin:20px 0;
}
.gallery img{
 width:100%;height:180px;object-fit:cover;
 border-radius:15px;
}
.photo-box{
 background:#fff0f8;border:1px dashed #d77bb5;
 border-radius:15px;padding:12px;
}
.small{font:12px Arial;line-height:1.6;color:#986c91}
.error{color:#c62868;font-size:14px}
@media(max-width:420px){
 .countdown{gap:5px}
 .time{padding:13px 2px}
 .time strong{font-size:23px}
 .time span{font-size:9px}
}
</style>
</head>

<body>

<div class="butterfly b1">🦋</div>
<div class="butterfly b2">🦋</div>
<div class="butterfly b3">🦋</div>

<!-- PASSWORD SCREEN -->
<section id="login">
 <div class="card">
  <p>✧ A PRIVATE LITTLE WORLD ✧</p>
  <h1>Elizabeth's Pink Paradise 💗</h1>
  <p class="script">A special surprise is waiting...</p>
  <p>Enter your secret passcode to enter.</p>

  <input
   type="password"
   id="passcode"
   placeholder="Enter passcode"
   inputmode="numeric"
   maxlength="6"
   autocomplete="off"
  >

  <br>
  <button onclick="enterSite()">Unlock My Surprise 💌</button>

  <p id="loginError" class="error"></p>
  <p class="small">A little world made with love 🦋</p>
 </div>
</section>

<!-- COUNTDOWN ONLY FOR ELIZABETH BEFORE RELEASE -->
<section id="countdown" class="hidden">
 <div class="card">
  <p>✧ SOMETHING BEAUTIFUL IS WAITING ✧</p>
  <h2>Counting Down to Your Special Day</h2>
  <p class="script">The world is getting ready to celebrate you, Lizzy! 🦋</p>

  <div class="countdown">
   <div class="time"><strong id="days">0</strong><span>Days</span></div>
   <div class="time"><strong id="hours">0</strong><span>Hours</span></div>
   <div class="time"><strong id="minutes">0</strong><span>Minutes</span></div>
   <div class="time"><strong id="seconds">0</strong><span>Seconds</span></div>
  </div>

  <p id="countMessage">
   Your beautiful surprise will unlock on December 9! 💕
  </p>
  <p class="script">Until then, keep smiling, my beautiful Lizzy. ❤️</p>
 </div>
</section>

<!-- MAIN WEBSITE -->
<div id="mainSite" class="hidden">

<section id="welcome">
 <div class="card">
  <p>✧ A LITTLE WORLD MADE JUST FOR YOU ✧</p>
  <h1>Elizabeth 💗</h1>
  <p class="script">My beautiful Lizzy...</p>
  <p>Some people make life more beautiful just by being in it. This little surprise is made especially for you, with love.</p>
  <button onclick="show('birthday')">Open Your Surprise 💌</button>
  <p>🦋 ✨ 💕 ✨ 🦋</p>
 </div>
</section>

<section id="birthday" class="hidden">
 <div class="card">
  <p>THE MOST SPECIAL DAY</p>
  <div class="cake">🎂</div>
  <h1>Happy Birthday,<br>My Beautiful Lizzy!</h1>
  <p class="script">December 9 — a day as special as you.</p>
  <p>You are not just a beautiful part of my life; you are one of the reasons my life feels beautiful.</p>
  <button onclick="show('countdown')">Your Live Countdown ⏳</button>
  <button onclick="show('letter')">My Love Letter 💗</button>
 </div>
</section>

<section id="letter" class="hidden">
 <div class="card">
  <p>A MESSAGE FROM MY HEART</p>
  <h2>My Dearest Elizabeth</h2>
  <div class="letter">
   <p>My love,</p>
   <p>I may not always find the perfect words to explain how much you mean to me, but I hope you always feel how special you are to me. Your smile makes ordinary moments beautiful, and your presence brings warmth to my life.</p>
   <p>I am grateful for every conversation, every laugh, every little memory, and every moment we share. I hope you never forget how precious you are and how much happiness you deserve.</p>
   <p>On your birthday, I wish you endless happiness, good health, peace of mind, success, and the courage to follow every dream in your heart. May life surprise you with beautiful opportunities, wonderful memories, and countless reasons to smile.</p>
   <p>Whatever challenges come your way, I hope you always find the strength to overcome them. Keep shining, keep smiling, and never stop being the wonderful person you are.</p>
   <p>Thank you for being you. You are precious to me, today and always.</p>
   <p class="script">With all my love, always. ❤️</p>
  </div>
  <button onclick="show('wishes')">Your Birthday Wishes ✨</button>
 </div>
</section>

<section id="wishes" class="hidden">
 <div class="card">
  <p>MY WISHES FOR YOU</p>
  <h2>May Your Life Be Magical 🌷</h2>
  <p>May your heart always be peaceful, your smile always be bright, and your dreams turn into beautiful realities.</p>
  <p>May every new chapter bring success, confidence, happiness, and people who genuinely care about you.</p>
  <p>May God bless you with good health, strength, protection, and a future filled with beautiful moments.</p>
  <p class="script">You deserve all the love and happiness in this world. 💗</p>
  <button onclick="show('memories')">Our Memory Corner 📸</button>
 </div>
</section>

<section id="memories" class="hidden">
 <div class="card">
  <p>OUR BEAUTIFUL STORY</p>
  <h2>Little Moments, Big Memories</h2>
  <p>Every smile, every laugh, and every little moment can become a beautiful memory.</p>

  <div class="gallery">
   <div class="photo-box">
    <input type="file" accept="image/*" onchange="preview(this)">
    <p class="small">Choose a photo</p>
   </div>
   <div class="photo-box">
    <input type="file" accept="image/*" onchange="preview(this)">
    <p class="small">Choose a photo</p>
   </div>
   <div class="photo-box">
    <input type="file" accept="image/*" onchange="preview(this)">
    <p class="small">Choose a photo</p>
   </div>
   <div class="photo-box">
    <input type="file" accept="image/*" onchange="preview(this)">
    <p class="small">Choose a photo</p>
   </div>
  </div>

  <p class="small">
   Photo previews are local to the browser. To share photos with other visitors,
   add publicly hosted image links to the HTML.
  </p>
  <button onclick="show('final')">One Last Surprise 💝</button>
 </div>
</section>

<section id="final" class="hidden">
 <div class="card">
  <div style="font-size:65px">💗🦋✨🦋💗</div>
  <h1>Keep Shining, Lizzy!</h1>
  <p class="script">The world is more beautiful with you in it.</p>
  <p>Happy Birthday, Elizabeth. May your life always be filled with love, laughter, blessings, and beautiful dreams.</p>
  <h2>Forever Special ❤️</h2>
  <button onclick="show('welcome')">Experience Again ↺</button>
 </div>
</section>

</div>

<script>
// YOUR OWNER PASSWORD
const OWNER_PASSWORD = "130793";

// ELIZABETH'S PASSWORD
const LIZZY_PASSWORD = "123456";

// Birthday unlock time: December 9, 2026, midnight in India
const RELEASE_AT = new Date("2026-12-09T00:00:00+05:30");

let accessRole = null;

function hideAll(){
 document.querySelectorAll("section").forEach(section=>{
  section.classList.add("hidden");
 });
 document.getElementById("mainSite").classList.add("hidden");
}

function show(id){
 document.querySelectorAll("#mainSite section").forEach(section=>{
  section.classList.add("hidden");
 });
 document.getElementById("mainSite").classList.remove("hidden");
 document.getElementById(id).classList.remove("hidden");
 window.scrollTo({top:0,behavior:"smooth"});
}

function openFullWebsite(){
 hideAll();
 document.getElementById("mainSite").classList.remove("hidden");
 show("welcome");
}

function enterSite(){
 const entered = document.getElementById("passcode").value;
 const error = document.getElementById("loginError");

 if(entered === OWNER_PASSWORD){
  accessRole = "owner";
  localStorage.setItem("lizzyAccessRole","owner");
  openFullWebsite();
  return;
 }

 if(entered === LIZZY_PASSWORD){
  accessRole = "lizzy";
  localStorage.setItem("lizzyAccessRole","lizzy");

  if(new Date() >= RELEASE_AT){
   openFullWebsite();
  }else{
   hideAll();
   document.getElementById("countdown").classList.remove("hidden");
   updateCountdown();
  }
  return;
 }

 error.textContent = "Incorrect passcode. Please try again. 💗";
 document.getElementById("passcode").value = "";
}

function checkSavedAccess(){
 const savedRole = localStorage.getItem("lizzyAccessRole");

 if(savedRole === "owner"){
  accessRole = "owner";
  openFullWebsite();
 }else if(savedRole === "lizzy"){
  accessRole = "lizzy";

  if(new Date() >= RELEASE_AT){
   openFullWebsite();
  }else{
   hideAll();
   document.getElementById("countdown").classList.remove("hidden");
   updateCountdown();
  }
 }else{
  hideAll();
  document.getElementById("login").classList.remove("hidden");
 }
}

function updateCountdown(){
 const now = new Date();

 // Elizabeth's countdown is for the first unlock date.
 const target = RELEASE_AT;
 const diff = target - now;

 if(diff <= 0){
  if(accessRole === "lizzy"){
   openFullWebsite();
  }
  return;
 }

 const day = 86400000;
 const hour = 3600000;
 const minute = 60000;

 document.getElementById("days").textContent =
  Math.floor(diff/day);

 document.getElementById("hours").textContent =
  Math.floor((diff%day)/hour);

 document.getElementById("minutes").textContent =
  Math.floor((diff%hour)/minute);

 document.getElementById("seconds").textContent =
  Math.floor((diff%minute)/1000);
}

function preview(input){
 const file = input.files[0];
 if(!file)return;

 const reader = new FileReader();

 reader.onload = function(e){
  const img = document.createElement("img");
  img.src = e.target.result;
  img.alt = "Selected memory";
  input.parentElement.innerHTML = "";
  input.parentElement.appendChild(img);
 };

 reader.readAsDataURL(file);
}

function createSparkle(){
 const sparkle = document.createElement("span");
 sparkle.className = "sparkle";
 sparkle.textContent = ["✨","💕","💗","🌸"][
  Math.floor(Math.random()*4)
 ];
 sparkle.style.left = Math.random()*100 + "vw";
 sparkle.style.fontSize = (14+Math.random()*16) + "px";
 sparkle.style.animationDuration = (6+Math.random()*6) + "s";

 document.body.appendChild(sparkle);
 setTimeout(()=>sparkle.remove(),12000);
}

document.getElementById("passcode").addEventListener("keydown",function(e){
 if(e.key === "Enter") enterSite();
});

checkSavedAccess();
updateCountdown();
setInterval(updateCountdown,1000);
setInterval(createSparkle,900);
</script>

</body>
</html>
