# love-
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Propose Day</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body{
margin:0;
height:100vh;
background:linear-gradient(135deg,#ff5f6d,#ffc371);
display:flex;
justify-content:center;
align-items:center;
overflow:hidden;
font-family:Arial;
color:white;
}
#tap{
font-size:2rem;
animation:blink 1.2s infinite;
}
@keyframes blink{50%{opacity:.3}}
#box{display:none;text-align:center}
h1{font-size:3rem}
.heart{
position:absolute;
animation:float 5s linear infinite;
}
@keyframes float{
0%{bottom:-10%;opacity:1}
100%{bottom:110%;opacity:0}
}
</style>
</head>
<body onclick="start()">

<div id="tap">💖 Tap to Open 💖</div>

<div id="box">
<h1>💍 Kissmiss 💍</h1>
<p>I love you ❤️</p>
</div>

<script>
function start(){
document.getElementById("tap").style.display="none";
document.getElementById("box").style.display="block";
setInterval(()=>{
let h=document.createElement("div");
h.className="heart";
h.innerHTML="❤️💖💕";
h.style.left=Math.random()*100+"vw";
document.body.appendChild(h);
setTimeout(()=>h.remove(),5000);
},300);
}
</script>

</body>
</html>
