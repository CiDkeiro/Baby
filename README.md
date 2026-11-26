
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Little Something For You ❤️</title>

<style>
*{box-sizing:border-box}
body{
 margin:0;padding:20px;min-height:100vh;
 background:linear-gradient(145deg,#100810,#351324,#160b18);
 color:white;text-align:center;font-family:Georgia,serif;
}
h1{color:#ffb2ca;margin-top:30px}
.sub{color:#d9b6c4}
.scene{
 position:relative;height:230px;max-width:450px;
 margin:35px auto 15px;
 background:linear-gradient(120deg,#240e24,#48162f);
 border:1px solid #a94d75;border-radius:20px;
 overflow:hidden;
}
.bow{position:absolute;left:7%;top:85px;font-size:65px}
.arrow{position:absolute;left:24%;top:105px;font-size:35px;opacity:0}
.target{position:absolute;right:9%;top:72px;font-size:90px}
.fly{animation:shoot 1s ease-in forwards}
@keyframes shoot{
 from{left:24%;opacity:1}
 to{left:76%;opacity:1}
}
button{
 background:#b83d70;border:1px solid #ff9cbd;
 color:white;padding:14px 25px;border-radius:30px;
 font-size:15px;margin:12px;cursor:pointer;
}
.letter{
 display:none;max-width:480px;margin:25px auto;
 padding:25px;background:#fff4f7;color:#422331;
 border-radius:15px;text-align:left;line-height:1.85;
 animation:show 1s;
}
.letter h2{text-align:center;color:#a52f61}
.signature{text-align:right}
.credit{
 text-align:center;color:#a52f61;
 margin-top:30px;padding-top:20px;
 border-top:1px solid #e9b8ca;
}
.credit strong{font-size:22px}
.heart{
 position:fixed;bottom:-30px;
 animation:float 5s linear forwards;
 pointer-events:none;
}
@keyframes float{
 to{transform:translateY(-110vh) rotate(360deg);opacity:0}
}
@keyframes show{
 from{opacity:0;transform:translateY(20px)}
 to{opacity:1;transform:translateY(0)}
}
</style>
</head>

<body>

<h1>Hey, You. ❤️</h1>
<p class="sub">I made a little something for you.</p>

<div class="scene">
 <div class="bow">🏹</div>
 <div class="arrow" id="arrow">➵❤️</div>
 <div class="target" id="target">🤍</div>
</div>

<p id="status">May gusto lang akong sabihin sa'yo.</p>
<button onclick="shoot()">Shoot the Arrow 🏹</button>

<div class="letter" id="letter">

<h2>Just A Little Letter 💌</h2>

<p>Hi, ikaw.</p>

<p>
Alam mo, may gusto lang talaga akong sabihin.
First, sorry kung lately medyo busy ako
at hindi ako masyadong nakakapagbigay ng time sa'yo.
</p>

<p>
Hindi naman sa ayaw kitang kausap or
hindi na ako interested. Minsan lang talaga
maraming kailangang asikasuhin, and I know
na hindi magandang dahilan yun para
makalimutan kong mag-update sa'yo.
</p>

<p>
I'm sorry kung may times na napaghintay kita
or hindi ako nakapag-reply agad.
I hope hindi mo naisip na wala akong pake,
because that's definitely not the case.
</p>

<p>
I know we're both living our own lives
and may kanya-kanya tayong ginagawa.
I don't expect you to always understand
my situation, but I hope you know
I'm trying to manage everything.
</p>

<p>
Honestly, I enjoy talking to you.
Kahit simpleng conversation lang,
it can make my day better.
Kaya ayokong isipin mong dahil lang
busy ako, hindi na kita gustong kausap.
</p>

<p>
I won't promise na lagi akong available,
because I don't want to make promises
na baka hindi ko rin magawa.
But I'll do my best to make time,
communicate better, and show you
that I genuinely care.
</p>

<p>
No pressure, okay? I just want us to
enjoy getting to know each other.
One step at a time lang. ❤️
</p>

<p>
And lastly, thank you for being patient
with me. I appreciate you more than
you probably realize.
</p>

<br>

<p class="signature">
Take care always,<br>
<strong>Your Baby ❤️</strong>
</p>

<div class="credit">
<p>Specially made with love by:</p>
<strong>Your Baby ❤️</strong>
<p>Just for you. 🌹</p>
</div>

<div style="text-align:center">
<button onclick="finalMessage()">One Last Thing... ❤️</button>
</div>

<h2 id="final"></h2>

</div>

<script>
let fired=false;

function shoot(){
 if(fired)return;
 fired=true;

 document.getElementById("arrow").classList.add("fly");
 document.getElementById("status").innerText=
 "Sending a little message from my heart...";

 setTimeout(()=>{
 document.getElementById("target").innerText="💘";
 document.getElementById("status").innerText="Delivered. ❤️";
 document.getElementById("letter").style.display="block";
 document.getElementById("letter").scrollIntoView({behavior:"smooth"});
 hearts();
 },1100);
}

function hearts(){
 for(let i=0;i<25;i++){
 setTimeout(()=>{
 let h=document.createElement("div");
 h.className="heart";
 h.innerText=["❤️","💕","🤍","💗"][Math.floor(Math.random()*4)];
 h.style.left=Math.random()*100+"vw";
 h.style.fontSize="22px";
 document.body.appendChild(h);
 setTimeout(()=>h.remove(),5000);
 },i*100);
 }
}

function finalMessage(){
 document.getElementById("final").innerHTML=
 "I hope you smiled kahit konti habang binabasa mo 'to. I'm happy na nakilala kita. Thank you for being you. ❤️";
 hearts();
}
</script>

</body>
</html>
