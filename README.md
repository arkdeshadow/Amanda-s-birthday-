<!DOCTYPE html>
<html>
<head>
<title>Happy Birthday Amanda Narh 🎂</title>

<style>
body{
margin:0;
overflow:hidden;
font-family:Arial;
text-align:center;
color:white;
background:linear-gradient(135deg,#ff6ec7,#6a5acd);
}

h1{
margin-top:60px;
font-size:55px;
}

p{
font-size:22px;
}

.object{
position:absolute;
bottom:-100px;
font-size:35px;
animation:floatUp linear infinite;
}

@keyframes floatUp{
from{transform:translateY(0);}
to{transform:translateY(-120vh);}
}

.confetti{
position:absolute;
font-size:20px;
animation:confettiFall linear forwards;
}

@keyframes confettiFall{
from{transform:translateY(-10vh);}
to{transform:translateY(110vh);}
}

.heart{
position:absolute;
font-size:25px;
animation:heartFall linear forwards;
}

@keyframes heartFall{
from{transform:translateY(-10vh);}
to{transform:translateY(110vh);}
}

.popup{
position:fixed;
top:50%;
left:50%;
transform:translate(-50%,-50%);
background:white;
color:black;
padding:25px;
border-radius:15px;
display:none;
}

.cake{
font-size:80px;
margin-top:20px;
animation:cakeBounce 2s infinite;
}

@keyframes cakeBounce{
0%{transform:translateY(0);}
50%{transform:translateY(-10px);}
100%{transform:translateY(0);}
}

button{
padding:10px 20px;
border:none;
border-radius:10px;
cursor:pointer;
}
</style>

</head>

<body>

<h1>🎉 Happy Birthday Amanda Narh 🎉</h1>

<p>
May your day be filled with happiness, laughter, love and beautiful memories.
You deserve the best birthday ever! 💖
</p>

<div class="cake">🎂🕯️</div>

<div class="popup" id="popup">
<h2>🎁 Birthday Surprise!</h2>
<p>Amanda, you are amazing and today is all about celebrating you! 💕</p>
<button onclick="closePopup()">Close</button>
</div>

<audio autoplay loop>
<source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3">
</audio>

<script>

function floating(symbol){
let obj=document.createElement("div");
obj.className="object";
obj.innerHTML=symbol;

obj.style.left=Math.random()*window.innerWidth+"px";
obj.style.animationDuration=(5+Math.random()*5)+"s";

document.body.appendChild(obj);

setTimeout(()=>{obj.remove();},10000);
}

setInterval(()=>{floating("🎈");},700);
setInterval(()=>{floating("🧸");},1500);


function confetti(){
let c=document.createElement("div");
c.className="confetti";
c.innerHTML="🎊";

c.style.left=Math.random()*window.innerWidth+"px";
c.style.animationDuration=(2+Math.random()*3)+"s";

document.body.appendChild(c);

setTimeout(()=>{c.remove();},4000);
}

setInterval(confetti,300);


function hearts(){
let h=document.createElement("div");
h.className="heart";
h.innerHTML="❤️";

h.style.left=Math.random()*window.innerWidth+"px";
h.style.animationDuration=(3+Math.random()*3)+"s";

document.body.appendChild(h);

setTimeout(()=>{h.remove();},5000);
}

setInterval(hearts,800);


setTimeout(()=>{
document.getElementById("popup").style.display="block";
},4000);

function closePopup(){
document.getElementById("popup").style.display="none";
}


setTimeout(()=>{
let msg=new SpeechSynthesisUtterance(
"Happy Birthday Amanda Narh. May your life be filled with happiness, love and success."
);
speechSynthesis.speak(msg);
},6000);

</script>

</body>
</html>
