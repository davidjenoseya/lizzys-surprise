
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#f8dce9">
<title>Elizabeth's Surprise 🦋</title>
<style>
*{box-sizing:border-box}
body{margin:0;min-height:100vh;display:grid;place-items:center;padding:15px;background:linear-gradient(135deg,#fff4fa,#eadcfb);font-family:Georgia,serif;color:#743b60}
.app{width:100%;max-width:440px;min-height:650px;background:#ffffffdf;border:1px solid white;border-radius:30px;box-shadow:0 15px 50px #9c547533;padding:25px 20px;display:flex;flex-direction:column;text-align:center;align-items:center;position:relative;overflow:hidden}
h1{color:#a7477c;font-size:2.2rem}
p{font-size:1.1rem;line-height:1.7}
.screen{display:none;flex:1;width:100%;flex-direction:column;justify-content:center;align-items:center;animation:fade .6s}
.screen.active{display:flex}
@keyframes fade{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:translateY(0)}}
.butterfly{font-size:100px;animation:float 3s infinite}
@keyframes float{50%{transform:translateY(-15px) rotate(8deg)}}
.emoji{font-size:75px}
.note{background:#fff4fa;border:1px solid #f0c9dc;border-radius:20px;padding:20px;line-height:1.9;font-size:17px}
.gallery{display:grid;grid-template-columns:1fr 1fr;gap:10px;width:100%;margin:15px 0}
.photo{min-height:130px;background:#f8e7ef;border-radius:15px;overflow:hidden;display:grid;place-items:center}
.photo img{width:100%;height:150px;object-fit:cover}
input{display:none}
button,.upload{border:0;border-radius:30px;padding:14px 22px;background:linear-gradient(100deg,#d978a7,#a94c83);color:white;font-size:16px;font-weight:bold;margin:10px;cursor:pointer}
.secondary{background:white;color:#a7477c;border:1px solid #edc4d9}
.footer{font:12px Arial;margin-top:auto;opacity:.65;padding-top:15px}
</style>
</head>
<body>
<main class="app">

<section class="screen active" id="welcome">
<div class="butterfly">🦋</div>
<h1>A Little Surprise for Elizabeth</h1>
<p>Someone made a tiny world just for you. 💗</p>
<button onclick="show('birthday')">Tap the butterfly 🦋</button>
</section>

<section class="screen" id="birthday">
<div class="emoji">🎂🎈</div>
<h1>Happy Birthday, Elizabeth!</h1>
<p>Today is all about you, my favourite person!</p>
<button onclick="show('letter')">Open Your Surprise 💌</button>
</section>

<section class="screen" id="letter">
<div class="emoji">💌</div>
<h1>A Note For You</h1>
<div class="note">
You make my ordinary days special. Your smile is my favourite thing, and I'm lucky to have you in my life.
<br><br>
<strong>Hey, stop being too cute, the app might freeze! 😂</strong>
</div>
<button onclick="show('gallery')">Our Journey 📸</button>
</section>

<section class="screen" id="gallery">
<div class="emoji">📷</div>
<h1>Our Journey</h1>
<p>Add your favourite memories here. ❤️</p>
<label class="upload" for="photos">＋ Add Photos</label>
<input id="photos" type="file" accept="image/*" multiple>
<div class="gallery" id="galleryGrid">
<div class="photo">Our first memory 💗</div>
<div class="photo">That lovely smile 😊</div>
</div>
<button onclick="show('final')">One Last Thing ❤️</button>
</section>

<section class="screen" id="final">
<div class="emoji">🦋💖</div>
<h1>Forever My Favourite Person</h1>
<p>Happy Birthday once again, Elizabeth. Keep smiling, beautiful! ❤️</p>
<button class="secondary" onclick="show('welcome')">Replay Our Little Story ↻</button>
</section>

<div class="footer">Made with love · Elizabeth's Surprise 🦋</div>
</main>

<script>
function show(id){
 document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active'));
 document.getElementById(id).classList.add('active');
}
document.getElementById('photos').addEventListener('change',function(){
 const grid=document.getElementById('galleryGrid');
 for(const file of this.files){
  if(!file.type.startsWith('image/'))continue;
  const img=document.createElement('img');
  img.src=URL.createObjectURL(file);
  img.alt='A memory';
  const card=document.createElement('div');
  card.className='photo';
  card.appendChild(img);
  grid.appendChild(card);
 }
});
</script>
</body>
</html>

