
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#f8c4e3">
<title>Elizabeth's Pink Paradise 💗</title>

<style>
:root{
 --pink:#ed80bb;
 --light:#fff0f8;
 --purple:#a66ac8;
 --dark:#71365e;
 --gold:#d6ad68;
}
*{box-sizing:border-box}
body{
 margin:0;font-family:Georgia,serif;color:var(--dark);
 background:linear-gradient(135deg,#ffe2f1,#eadcff,#fff1f8);
 text-align:center;min-height:100vh;overflow-x:hidden;
}
button,input,textarea{font:inherit}
button{
 border:0;border-radius:30px;padding:13px 23px;margin:7px;
 color:white;background:linear-gradient(120deg,#ed75b9,#a77be8);
 cursor:pointer;box-shadow:0 5px 15px #c77dbb55;
}
button:hover{filter:brightness(1.06);transform:translateY(-2px)}
input,textarea{
 width:100%;padding:12px;border:1px solid #e9b8d6;
 border-radius:12px;margin:7px 0;background:white;color:#71365e;
}
textarea{min-height:75px}
section{
 min-height:100vh;display:flex;align-items:center;
 justify-content:center;padding:28px 15px;
}
.card{
 width:min(760px,100%);padding:30px 22px;
 background:#ffffffed;border:2px solid white;
 border-radius:27px;box-shadow:0 12px 45px #b66caa55;
}
h1{font-size:clamp(36px,8vw,65px);color:#d84d9e;margin:15px 0}
h2{font-size:clamp(26px,6vw,42px);color:#bd4c98}
p{font-size:17px;line-height:1.8}
.script{font-style:italic;color:#a14c8c;font-size:21px}
.small{font:12px Arial;line-height:1.6;color:#986c91}
.hidden{display:none!important}
.butterfly{
 position:fixed;z-index:5;pointer-events:none;font-size:30px;
 animation:fly 8s ease-in-out infinite;
}
.b1{top:12%;left:7%}
.b2{top:32%;right:8%;animation-delay:2s}
.b3{bottom:12%;left:15%;animation-delay:4s}
@keyframes fly{
 0%,100%{transform:translateY(0) rotate(-12deg)}
 50%{transform:translateY(-35px) rotate(15deg)}
}
.sparkle{position:fixed;pointer-events:none;z-index:4;animation:rise 8s linear forwards}
@keyframes rise{
 from{transform:translateY(100vh);opacity:0}
 20%{opacity:1}
 to{transform:translateY(-100vh);opacity:0}
}
.cake{font-size:100px;cursor:pointer;user-select:none;touch-action:pan-y}
.cake:active{transform:scale(.92)}
.countdown{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin:25px 0}
.time{background:#fff0f8;padding:16px 4px;border-radius:15px;border:1px solid #f1c3df}
.time strong{display:block;font:bold 30px Arial;color:#d34c9b}
.time span{font:11px Arial;text-transform:uppercase}
.letter{background:#fff8fc;padding:22px;border-radius:18px;text-align:left;border-left:4px solid #e38abd}
.gallery{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin:20px 0}
.photo{
 background:#fff0f8;border:1px dashed #d77bb5;
 border-radius:15px;padding:10px;min-height:160px;
 display:flex;flex-direction:column;justify-content:center;
}
.photo img{width:100%;height:180px;object-fit:cover;border-radius:12px}
.photo p{font-size:14px;margin:7px}
.admin{text-align:left}
.admin h3{color:#bd4c98}
.chatbox{
 height:220px;overflow-y:auto;background:#fff4fa;
 border:1px solid #efc4df;border-radius:15px;padding:12px;text-align:left;
}
.msg{padding:9px 12px;border-radius:13px;margin:8px 0;background:white;max-width:90%}
.msg.me{margin-left:auto;background:#f8d9ec}
#site{background-size:cover;background-position:center}
@media(max-width:420px){
 .countdown{gap:5px}.time{padding:12px 2px}
 .time strong{font-size:23px}.time span{font-size:9px}
 .gallery{gap:8px}
}
</style>
</head>

<body id="site">

<div class="butterfly b1">🦋</div>
<div class="butterfly b2">🦋</div>
<div class="butterfly b3">🦋</div>

<!-- LOGIN -->
<section id="login">
 <div class="card">
  <p>✧ A PRIVATE WORLD MADE WITH LOVE ✧</p>
  <h1>Pink Paradise 💗</h1>
  <p class="script">Welcome to Elizabeth's beautiful world</p>
  <input id="password" type="password" inputmode="numeric"
   placeholder="Enter your password">
  <button onclick="login()">Enter My World 💌</button>
  <p id="loginError" class="small"></p>
  <p class="small">A special place filled with love, memories and butterflies 🦋</p>
 </div>
</section>

<!-- OWNER -->
<section id="owner" class="hidden">
 <div class="card admin">
  <h1>Welcome, Owner 💗</h1>
  <p class="script">Your personal birthday control room</p>
  <h3>Edit the birthday messages</h3>

  <label>Opening birthday heading</label>
  <input id="editTitle">
  <label>Romantic paragraph</label>
  <textarea id="editLove"></textarea>
  <label>Funny note</label>
  <textarea id="editFunny"></textarea>
  <label>Final birthday wish</label>
  <textarea id="editFinal"></textarea>

  <h3>Background image</h3>
  <label>Paste a public image URL</label>
  <input id="backgroundURL" placeholder="https://...">
  <button onclick="applyBackground()">Apply background</button>
  <button onclick="document.getElementById('backgroundFile').click()">Choose background from phone</button>
  <input id="backgroundFile" type="file" accept="image/*" onchange="localBackground(this)" hidden>

  <h3>Preview</h3>
  <button onclick="saveText()">Save my edits</button>
  <button onclick="show('birthday')">Preview birthday website</button>
  <button onclick="show('login')">Back to login</button>
  <button onclick="logout()">Logout</button>

  <p class="small">
   Owner edits are saved in this browser. To publish them for Elizabeth,
   update the website file on GitHub and commit your changes.
  </p>
 </div>
</section>

<!-- ADVANCE BIRTHDAY / COUNTDOWN -->
<section id="advance" class="hidden">
 <div class="card">
  <p>💗 A SPECIAL MESSAGE FOR YOU 💗</p>
  <h1>Advance Happy Birthday, Lizzy!</h1>
  <p class="script">My beautiful sweetheart 🦋</p>
  <p>Every second brings us closer to celebrating you, Lizzy.
  Your special day is almost here, and I hope it brings you
  countless smiles, beautiful memories and endless happiness.</p>

  <h2>Your Birthday Countdown</h2>
  <div class="countdown">
   <div class="time"><strong id="days">0</strong><span>Days</span></div>
   <div class="time"><strong id="hours">0</strong><span>Hours</span></div>
   <div class="time"><strong id="minutes">0</strong><span>Minutes</span></div>
   <div class="time"><strong id="seconds">0</strong><span>Seconds</span></div>
  </div>
  <p id="countMessage">Counting every moment until your special day! 💕</p>
  <button onclick="logout()">Back to login</button>
 </div>
</section>

<!-- BIRTHDAY HOME -->
<section id="birthday" class="hidden">
 <div class="card">
  <p>✧ THE MOST BEAUTIFUL DAY ✧</p>
  <h1 id="birthdayTitle">Happy Birthday, My Sweetheart! 💗</h1>
  <p class="script">My beautiful Elizabeth, my favourite blessing.</p>
  <p id="loveText"></p>
  <button onclick="show('cake')">Cut Your Birthday Cake 🎂</button>
  <button onclick="show('memories')">Our Memories 📸</button>
  <button onclick="show('wishes')">My Wishes for You 🌷</button>
  <button onclick="show('ai')">Ask Lizzy AI 💬</button>
  <button onclick="show('login')">Back to login</button>
 </div>
</section>

<!-- CAKE -->
<section id="cake" class="hidden">
 <div class="card">
  <p>MAKE A WISH, MY LOVE!</p>
  <h1>Your Birthday Cake 🎂</h1>
  <p>Tap the cake or swipe left and right to cut it!</p>
  <div class="cake" id="cakeEmoji"
   ontouchstart="cakeTouchStart(event)"
   ontouchend="cakeTouchEnd(event)"
   onclick="cutCake()">🎂</div>
  <p id="cakeMessage" class="script">Make your beautiful wish, Lizzy!</p>
  <button onclick="cutCake()">Cut the cake ✨</button>
  <button onclick="show('memories')">Continue 💗</button>
 </div>
</section>

<!-- AGE CELEBRATION -->
<section id="celebration" class="hidden">
 <div class="card">
  <div style="font-size:65px">🎉💗🦋🎉</div>
  <h1>Congratulations!</h1>
  <h2>Welcome to Your 22th Year!</h2>
  <p class="script">Another beautiful chapter begins, Elizabeth!</p>
  <p>May this new chapter bring you confidence, happiness,
  success and all the dreams your heart wishes for.</p>
  <button onclick="show('memories')">See Our Memories 📸</button>
 </div>
</section>

<!-- MEMORIES -->
<section id="memories" class="hidden">
 <div class="card">
  <h1>Our Beautiful Memories 💞</h1>
  <p class="script">Every picture tells a little story.</p>
  <div class="gallery" id="gallery"></div>
  <button onclick="show('wishes')">Continue 💗</button>
 </div>
</section>

<!-- WISHES -->
<section id="wishes" class="hidden">
 <div class="card">
  <h1>My Wishes for You 🌷</h1>
  <p>May your smile never fade, your heart always find peace,
  and your dreams become beautiful realities.</p>
  <p>May God bless you with good health, protection, success
  and countless reasons to smile.</p>
  <p>May every new day bring you closer to the life you dream of.
  You deserve all the beautiful things in this world.</p>
  <h2>Forever Special ❤️</h2>
  <button onclick="show('final')">One Last Surprise 💝</button>
 </div>
</section>

<!-- FINAL -->
<section id="final" class="hidden">
 <div class="card">
  <div style="font-size:60px">💗🦋✨🦋💗</div>
  <h1>Keep Smiling, My Sweetheart!</h1>
  <p id="finalText"></p>
  <p class="script">I wish to create many more beautiful memories together. ❤️</p>
  <button onclick="show('ai')">Chat with Lizzy AI</button>
  <button onclick="show('birthday')">Start Again ↺</button>
 </div>
</section>

<!-- SIMPLE AI STYLE CHAT -->
<section id="ai" class="hidden">
 <div class="card">
  <h1>Lizzy AI 💗</h1>
  <p class="script">A little helper made for you.</p>
  <div class="chatbox" id="chatbox">
   <div class="msg">Hello Lizzy! 💕 Ask me something. I'm happy to help!</div>
  </div>
  <input id="chatInput" placeholder="Type your question...">
  <button onclick="chat()">Send 💌</button>
  <button onclick="show('birthday')">Back</button>
  <p class="small">This is an offline demo assistant with prepared replies, not a live internet AI.</p>
 </div>
</section>

<script>
const OWNER_PASSWORD="130793";
const LIZZY_PASSWORD="123456";
const BIRTHDAY_MONTH=11;
const BIRTHDAY_DAY=9;
const BIRTHDAY_YEAR=2026;

let currentRole="";
let cakeCuts=0;
let touchStartX=0;

const defaults={
 title:"Happy Birthday, My Sweetheart! 💗",
 love:`My beautiful Lizzy,

If I could give you one thing in life, it would be the ability to see yourself through my eyes. Then you would understand how precious and beautiful you are to me.

Your smile makes my ordinary days special. Your presence brings happiness into my life, and every little moment with you becomes a memory I want to keep forever.

I wish you endless happiness, good health, peace, success and the courage to follow every dream in your heart.

Thank you for being you. You are my favourite blessing, my sweetest thought and a beautiful part of my life.

Happy Birthday, my love. Always keep smiling. ❤️`,
 funny:"Don't stare at the screen for too long... your beautiful smile is freezing my display! 😂💗",
 final:"Happy Birthday, my beautiful Elizabeth! Keep smiling, follow your dreams, achieve everything your heart desires, and never forget how special you are. I hope we create many more beautiful memories together. ❤️"
};

function loadText(){
 const saved=JSON.parse(localStorage.getItem("lizzyTexts")||"{}");
 const data={...defaults,...saved};
 document.getElementById("editTitle").value=data.title;
 document.getElementById("editLove").value=data.love;
 document.getElementById("editFunny").value=data.funny;
 document.getElementById("editFinal").value=data.final;
 document.getElementById("birthdayTitle").textContent=data.title;
 document.getElementById("loveText").textContent=data.love;
 document.getElementById("finalText").textContent=data.final;
 document.getElementById("cakeMessage").textContent=data.funny;
}

function saveText(){
 const data={
  title:document.getElementById("editTitle").value,
  love:document.getElementById("editLove").value,
  funny:document.getElementById("editFunny").value,
  final:document.getElementById("editFinal").value
 };
 localStorage.setItem("lizzyTexts",JSON.stringify(data));
 loadText();
 alert("Your edits have been saved in this browser! 💗");
}

function show(id){
 document.querySelectorAll("section").forEach(s=>s.classList.add("hidden"));
 document.getElementById(id).classList.remove("hidden");
 window.scrollTo({top:0,behavior:"smooth"});
}

function login(){
 const pass=document.getElementById("password").value;
 document.getElementById("loginError").textContent="";
 if(pass===OWNER_PASSWORD){
  currentRole="owner";
  loadText();
  show("owner");
 }else if(pass===LIZZY_PASSWORD){
  currentRole="lizzy";
  updateCountdown();
  if(new Date()>=new Date(BIRTHDAY_YEAR,BIRTHDAY_MONTH,BIRTHDAY_DAY)){
   show("birthday");
  }else{
   show("advance");
  }
 }else{
  document.getElementById("loginError").textContent="Incorrect password. Please try again.";
 }
 document.getElementById("password").value="";
}

function logout(){
 currentRole="";
 document.getElementById("password").value="";
 show("login");
}

function updateCountdown(){
 let now=new Date();
 let target=new Date(BIRTHDAY_YEAR,BIRTHDAY_MONTH,BIRTHDAY_DAY,0,0,0);
 if(now>=target){
  ["days","hours","minutes","seconds"].forEach(id=>
   document.getElementById(id).textContent="0");
  document.getElementById("countMessage").textContent=
   "Happy Birthday, Lizzy! Your surprise is ready! 💗";
  return;
 }
 let diff=target-now;
 document.getElementById("days").textContent=Math.floor(diff/86400000);
 document.getElementById("hours").textContent=Math.floor(diff%86400000/3600000);
 document.getElementById("minutes").textContent=Math.floor(diff%3600000/60000);
 document.getElementById("seconds").textContent=Math.floor(diff%60000/1000);
}
updateCountdown();
setInterval(updateCountdown,1000);

function cutCake(){
 cakeCuts++;
 document.getElementById("cakeEmoji").textContent=
  cakeCuts===1?"🍰":"🎂";
 if(cakeCuts===1){
  document.getElementById("cakeMessage").textContent=
   "Yay! You cut your birthday cake! 🎉";
  setTimeout(()=>show("celebration"),1200);
 }else{
  document.getElementById("cakeMessage").textContent=
   "Your birthday wish is on its way! 💗";
 }
}
function cakeTouchStart(e){touchStartX=e.changedTouches[0].screenX}
function cakeTouchEnd(e){
 let distance=e.changedTouches[0].screenX-touchStartX;
 if(Math.abs(distance)>30)cutCake();
}

function makeGallery(){
 const captions=[
  "Your smile is my favourite photograph. 💗",
  "Every moment with you is special. 🦋",
  "A beautiful memory I will always treasure.",
  "You make ordinary days magical. ✨",
  "My favourite person, my sweetest blessing.",
  "A little picture, a lot of love. ❤️",
  "May we create a thousand more memories."
 ];
 const gallery=document.getElementById("gallery");
 gallery.innerHTML="";
 captions.forEach((caption,i)=>{
  const box=document.createElement("div");
  box.className="photo";
  const saved=localStorage.getItem("lizzyPhoto"+i);
  if(saved){
   const img=document.createElement("img");
   img.src=saved;img.alt="Memory "+(i+1);
   box.appendChild(img);
  }else{
   const icon=document.createElement("div");
   icon.textContent="📸";
   icon.style.fontSize="35px";
   box.appendChild(icon);
  }
  const p=document.createElement("p");
  p.textContent=caption;
  box.appendChild(p);
  if(currentRole==="owner"){
   const input=document.createElement("input");
   input.type="file";input.accept="image/*";
   input.onchange=function(){
    const file=input.files[0];
    if(!file)return;
    const reader=new FileReader();
    reader.onload=function(e){
     try{
      localStorage.setItem("lizzyPhoto"+i,e.target.result);
      makeGallery();
     }catch(err){
      alert("This photo is too large for browser storage. Use a smaller image.");
     }
    };
    reader.readAsDataURL(file);
   };
   box.appendChild(input);
   const remove=document.createElement("button");
   remove.textContent="Remove photo";
   remove.onclick=function(){
    localStorage.removeItem("lizzyPhoto"+i);
    makeGallery();
   };
   box.appendChild(remove);
  }
  gallery.appendChild(box);
 });
}

function applyBackground(){
 const url=document.getElementById("backgroundURL").value.trim();
 if(url){
  document.body.style.backgroundImage=`url("${url}")`;
  document.body.style.backgroundSize="cover";
  document.body.style.backgroundAttachment="fixed";
 }
}
function localBackground(input){
 const file=input.files[0];
 if(!file)return;
 const reader=new FileReader();
 reader.onload=function(e){
  document.body.style.backgroundImage=`url("${e.target.result}")`;
  document.body.style.backgroundSize="cover";
  document.body.style.backgroundAttachment="fixed";
 };
 reader.readAsDataURL(file);
}

function createSparkle(){
 const s=document.createElement("span");
 s.className="sparkle";
 s.textContent=["✨","💕","💗","🌸","🦋"][Math.floor(Math.random()*5)];
 s.style.left=Math.random()*100+"vw";
 s.style.fontSize=(14+Math.random()*17)+"px";
 s.style.animationDuration=(6+Math.random()*6)+"s";
 document.body.appendChild(s);
 setTimeout(()=>s.remove(),12000);
}
setInterval(createSparkle,900);

function chat(){
 const input=document.getElementById("chatInput");
 const question=input.value.trim();
 if(!question)return;
 const box=document.getElementById("chatbox");
 const mine=document.createElement("div");
 mine.className="msg me";mine.textContent=question;
 box.appendChild(mine);
 const q=question.toLowerCase();
 let answer="That's an interesting question! Keep smiling, Lizzy. 💗";
 if(q.includes("birthday"))answer="Your birthday is December 9! Get ready for a beautiful celebration! 🎂";
 else if(q.includes("love"))answer="You deserve genuine love, kindness and happiness. Never forget how special you are! ❤️";
 else if(q.includes("sad"))answer="Take a deep breath. You are stronger than you think. Give yourself some kindness today. 🌷";
 else if(q.includes("dream"))answer="Believe in yourself and keep moving towards your dreams. You can do wonderful things! ✨";
 else if(q.includes("smile"))answer="Your smile is priceless. Keep shining! 😊";
 else if(q.includes("help"))answer="I'm your little birthday helper. You can ask me about birthday wishes, encouragement or happy thoughts! 💕";
 const reply=document.createElement("div");
 reply.className="msg";reply.textContent=answer;
 box.appendChild(reply);
 box.scrollTop=box.scrollHeight;
 input.value="";
}

loadText();
makeGallery();
</script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Beautiful Memories Admin</title>

<style>
body {
  font-family: Arial, sans-serif;
  background: #fff0f7;
  padding: 20px;
  color: #713b59;
}

.container {
  max-width: 850px;
  margin: auto;
  background: white;
  padding: 22px;
  border-radius: 18px;
  box-shadow: 0 5px 20px #e7b5d0;
}

h1 { text-align: center; color: #e66ba7; }

.upload {
  display: block;
  margin: 20px auto;
  padding: 14px;
  background: #ffe0ef;
  border-radius: 12px;
  width: 90%;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 15px;
}

.card {
  background: #fff5fa;
  padding: 10px;
  border-radius: 12px;
}

.card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  border-radius: 10px;
}

.card input {
  width: 95%;
  margin-top: 8px;
  padding: 7px;
}

button {
  background: #e66ba7;
  color: white;
  border: none;
  padding: 10px 15px;
  border-radius: 8px;
  cursor: pointer;
  margin: 5px;
}

button:disabled {
  opacity: .5;
}

#status {
  text-align: center;
  margin: 15px;
}
</style>
</head>

<body>

<div class="container">

<h1>💗 Beautiful Memories Admin</h1>
<p>Select up to 7 beautiful memories.</p>

<input class="upload"
 type="file"
 id="photos"
 accept="image/*"
 multiple>

<div class="grid" id="preview"></div>

<p id="status">0 / 7 images selected</p>

<button onclick="savePhotos()">Save Memories</button>
<button onclick="clearPhotos()">Clear All</button>

</div>

<script>
let memories = [];

document.getElementById("photos")
.addEventListener("change", function(e) {

  const files = Array.from(e.target.files);

  if (files.length > 7) {
    alert("Please select only 7 images.");
    this.value = "";
    return;
  }

  memories.forEach(item =>
    URL.revokeObjectURL(item.url)
  );

  memories = files.map(file => ({
    file,
    url: URL.createObjectURL(file),
    caption: ""
  }));

  render();
});

function render() {
  const preview = document.getElementById("preview");
  preview.innerHTML = "";

  memories.forEach((item, index) => {
    preview.innerHTML += `
      <div class="card">
        <img src="${item.url}">
        <p>Memory ${index + 1}</p>
        <input
          placeholder="Write a caption..."
          value="${item.caption}"
          onchange="memories[${index}].caption=this.value">
        <button onclick="removePhoto(${index})">
          Delete
        </button>
      </div>
    `;
  });

  document.getElementById("status").innerText =
    memories.length + " / 7 images selected";
}

function removePhoto(index) {
  URL.revokeObjectURL(memories[index].url);
  memories.splice(index, 1);
  render();
}

function clearPhotos() {
  memories.forEach(item =>
    URL.revokeObjectURL(item.url)
  );
  memories = [];
  document.getElementById("photos").value = "";
  render();
}

function savePhotos() {
  if (memories.length !== 7) {
    alert("Please select all 7 images first.");
    return;
  }

  const data = memories.map(item => ({
    name: item.file.name,
    caption: item.caption,
    image: item.url
  }));

  localStorage.setItem(
    "beautifulMemories",
    JSON.stringify(data)
  );

  alert("Memories saved in this browser!");
}
</script>

</body>
</html>

