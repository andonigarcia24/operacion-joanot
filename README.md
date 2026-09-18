<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Operación Joanot | Mallorca 2026</title>


<style>

:root{
--turquoise:#00C9A7;
--blue:#00B8FF;
--yellow:#FFD93D;
--coral:#FF6B6B;
--white:#ffffff;
}

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Fredoka',sans-serif;
}

body{
background:linear-gradient(-45deg,#00C2C7,#FFD93D,#FF6B6B,#00B8FF);
background-size:400% 400%;
animation:gradient 12s ease infinite;
color:#222;
}

@keyframes gradient{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

.hero{
padding:60px 20px;
text-align:center;
color:white;
}

.hero h1{
font-size:3rem;
}

.hero p{
opacity:.95;
margin-top:10px;
}

.card{
background:rgba(255,255,255,.92);
backdrop-filter:blur(10px);
margin:16px;
padding:20px;
border-radius:25px;
box-shadow:0 10px 30px rgba(0,0,0,.15);
}

.section-title{
margin-bottom:15px;
font-size:1.5rem;
}

.stats{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:10px;
}

.stat{
background:#f5f5f5;
border-radius:15px;
padding:12px;
text-align:center;
}

.progress{
height:25px;
background:#ddd;
border-radius:50px;
overflow:hidden;
margin-top:10px;
}

.bar{
height:100%;
width:0;
background:linear-gradient(90deg,#00C9A7,#00B8FF);
transition:.4s;
}

.score{
font-size:40px;
text-align:center;
font-weight:bold;
color:#00C9A7;
}

.mission{
background:#f7f7f7;
padding:12px;
border-radius:15px;
margin-bottom:10px;
display:flex;
justify-content:space-between;
align-items:center;
gap:10px;
}

.btn{
border:none;
background:#00B8FF;
color:white;
padding:10px 14px;
border-radius:12px;
font-weight:bold;
}

.btn:hover{
cursor:pointer;
}

.alba-btn{
width:100%;
padding:18px;
font-size:24px;
background:#FF6B6B;
}

.bingo{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:8px;
}

.cell{
background:white;
padding:12px;
text-align:center;
border-radius:12px;
font-size:.8rem;
cursor:pointer;
}

.active{
background:#00C9A7;
color:white;
}

.team{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:10px;
}

.member{
background:#f5f5f5;
padding:12px;
border-radius:12px;
text-align:center;
font-weight:bold;
}

.castigo{
margin-top:15px;
background:#fff6d6;
padding:15px;
border-radius:15px;
font-weight:bold;
}

.badges{
display:flex;
flex-wrap:wrap;
gap:8px;
}

.badge{
background:#FFD93D;
padding:8px 12px;
border-radius:20px;
font-size:.85rem;
}

.timeline-item{
padding:10px 0;
border-left:4px solid #00B8FF;
padding-left:15px;
margin-bottom:8px;
}

footer{
padding:30px;
text-align:center;
color:white;
font-weight:bold;
}

.confetti{
position:fixed;
width:10px;
height:10px;
top:-10px;
pointer-events:none;
}

</style>
</head>

<body>

<div class="hero">
<h1>🏝️ OPERACIÓN JOANOT</h1>
<p>La Última Misión Antes del Matrimonio</p>
<p>Mallorca • Alcudia • Septiembre 2026</p>
</div>

<div class="card">
<h2 class="section-title">🎮 Perfil RPG</h2>

<p><b>Joan Muntané "Joanot"</b></p>
<p>Nivel 28 • Profesor Legendario</p>
<p>⚽ Barça Lover</p>
<p>⚡ Maestro Pokémon</p>
<p>🍬 Rey del Badulaque</p>
<p>👗 Calzonazos Supremo</p>
<p>❤️ Debilidad: Alba</p>
</div>

<div class="card">

<h2 class="section-title">⏳ Cuenta Atrás</h2>

<div class="stats">
<div class="stat"><h3 id="days">0</h3>Días</div>
<div class="stat"><h3 id="hours">0</h3>Horas</div>
<div class="stat"><h3 id="minutes">0</h3>Min</div>
<div class="stat"><h3 id="seconds">0</h3>Seg</div>
</div>

</div>

<div class="card">

<h2>🏆 Puntos de Experiencia</h2>

<div class="score" id="score">0</div>

<div class="progress">
<div class="bar" id="bar"></div>
</div>

</div>

<div class="card">

<h2>✅ Misiones Principales</h2>

<div id="missions"></div>

</div>

<div class="card">

<h2>🎯 Bingo Mallorca</h2>

<div class="bingo" id="bingo"></div>

</div>

<div class="card">

<h2>❤️ Maldición de Alba</h2>

<button class="btn alba-btn" onclick="alba()">
+ ALBA
</button>

<p style="margin-top:15px">
Invocaciones: <b id="albaCount">0</b>
</p>

<div class="castigo" id="albaCastigo">
Esperando invocación...
</div>

</div>

<div class="card">

<h2>🎲 Ruleta de Castigos</h2>

<button class="btn" onclick="girarRuleta()">
GIRAR
</button>

<div class="castigo" id="ruletaResultado">
Pulsa para girar
</div>

</div>

<div class="card">

<h2>🏅 Logros</h2>

<div class="badges" id="badges">
<div class="badge">Novio Novato</div>
</div>

</div>

<div class="card">

<h2>📍 Agenda Mallorca</h2>

<div class="timeline-item">
<b>Viernes</b><br>
Llegada • Piscina • Primeras cervezas
</div>

<div class="timeline-item">
<b>Sábado</b><br>
Misión principal • Pruebas • Fiesta
</div>

<div class="timeline-item">
<b>Domingo</b><br>
Supervivencia • Regreso
</div>

</div>

<div class="card">

<h2>👬 Equipo Organizador</h2>

<div class="team">

<div class="member">Andoni</div>
<div class="member">Arnau</div>

<div class="member">Dani</div>
<div class="member">Pol</div>

<div class="member">Merino</div>
<div class="member">Martos</div>

<div class="member">Manjón</div>
<div class="member">Marchal</div>

</div>

</div>

<footer>
OPERACIÓN JOANOT • 2026
</footer>

<script>

const missions = [
["📸 Foto con patrulla",50],
["❤️ 3 consejos matrimoniales",30],
["🎩 Caballero Mallorquín",40],
["🥃 Chupito sin manos",50],
["👱 Selfie Triple",60],
["🐻 Rascada Legendaria",40],
["🎭 Reencuentro Imposible",70],
["🎈 Operación Globo",80],
["✍️ Camiseta de la Fama",100],
["💍 Boss Final",150]
];

let score =
Number(localStorage.getItem("score")) || 0;

document.getElementById("score").innerText =
score;

updateBar();

missions.forEach(m=>{

const div=document.createElement("div");
div.className="mission";

div.innerHTML=`
<span>${m[0]} (${m[1]} pts)</span>
<button class="btn">Completar</button>
`;

div.querySelector("button").onclick=()=>{

score+=m[1];

localStorage.setItem("score",score);

document.getElementById("score").innerText=score;

updateBar();

confetti();

checkAchievements();

};

missionsDiv=document.getElementById("missions");
missionsDiv.appendChild(div);

});

function updateBar(){

let percent=Math.min((score/670)*100,100);

document.getElementById("bar").style.width=
percent+"%";

}

function checkAchievements(){

const badges=document.getElementById("badges");

if(score>=300 && !document.getElementById("ach300")){
let b=document.createElement("div");
b.id="ach300";
b.className="badge";
b.innerText="Maestro de Alcudia";
badges.appendChild(b);
}

if(score>=500 && !document.getElementById("ach500")){
let b=document.createElement("div");
b.id="ach500";
b.className="badge";
b.innerText="Superviviente Oficial";
badges.appendChild(b);
}

if(score>=670 && !document.getElementById("ach670")){
let b=document.createElement("div");
b.id="ach670";
b.className="badge";
b.innerText="Novio Legendario";
badges.appendChild(b);
}

}

const bingoItems = [
"Policía","Barco","Palmera","Perro",
"Alemán","Cóctel","Despedida","Tatuaje",
"Camarero","Atardecer","Bandera","Disfraz",
"Rubia","Morena","Pelirroja","Selfie"
];

bingoItems.forEach(item=>{

const cell=document.createElement("div");

cell.className="cell";

cell.innerText=item;

cell.onclick=()=>{
cell.classList.toggle("active");
};

document.getElementById("bingo")
.appendChild(cell);

});

const castigos=[

"Hablar como princesa",
"Pose Pokémon",
"Declarar amor al Barça",
"Presentarte como Joanota",
"Bailar 30 segundos",
"Pedir consejo matrimonial",
"Contar cómo conociste a Alba",
"Hacer reverencia a una palmera"

];

let albaCount=
Number(localStorage.getItem("alba")) || 0;

document.getElementById("albaCount").innerText=
albaCount;

function alba(){

albaCount++;

localStorage.setItem("alba",albaCount);

document.getElementById("albaCount").innerText=
albaCount;

document.getElementById("albaCastigo").innerText=
castigos[Math.floor(Math.random()*castigos.length)];

}

function girarRuleta(){

document.getElementById("ruletaResultado").innerText=
castigos[Math.floor(Math.random()*castigos.length)];

}

function countdown(){

const boda = new Date("2026-11-21");

const now = new Date();

const diff = boda - now;

document.getElementById("days").innerText =
Math.floor(diff/(1000*60*60*24));

document.getElementById("hours").innerText =
Math.floor(diff/(1000*60*60)%24);

document.getElementById("minutes").innerText =
Math.floor(diff/(1000*60)%60);

document.getElementById("seconds").innerText =
Math.floor(diff/1000%60);

}

setInterval(countdown,1000);

function confetti(){

for(let i=0;i<40;i++){

let c=document.createElement("div");

c.className="confetti";

c.style.left=Math.random()*100+"vw";
c.style.background=
["#FF6B6B","#FFD93D","#00B8FF","#00C9A7"][Math.floor(Math.random()*4)];

document.body.appendChild(c);

let y=-20;

let anim=setInterval(()=>{

y+=8;
c.style.top=y+"px";

if(y>window.innerHeight){
clearInterval(anim);
c.remove();
}

},20);

}

}

checkAchievements();

</script>

</body>
</html>
