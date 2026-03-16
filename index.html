<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<title>Rubik Timer</title>

<style>

body{
margin:0;
font-family:Arial;
background:linear-gradient(135deg,#0f2027,#203a43,#2c5364);
color:white;
text-align:center;
height:100vh;
overflow:hidden;
}

h1{
margin-top:20px;
color:#ffd93d;
}

#scramble{
font-size:28px;
margin-top:30px;
color:#ffffff;
letter-spacing:3px;
}

#timer{
font-size:140px;
margin-top:80px;
transition:0.2s;
}

.ready{
color:#00ff88;
}

#stats{
margin-top:20px;
font-size:22px;
}

button{
margin-top:15px;
padding:10px 18px;
border:none;
border-radius:8px;
background:#ff4d6d;
color:white;
font-size:16px;
cursor:pointer;
}

button:hover{
background:#ff1e4d;
}

#timesBox{

position:fixed;
left:20px;
bottom:20px;

background:rgba(0,0,0,0.4);
backdrop-filter:blur(6px);

padding:15px;
border-radius:10px;

width:220px;
max-height:300px;
overflow:auto;

}

#timesBox h3{
margin-top:0;
color:#ffd93d;
}

table{
width:100%;
border-collapse:collapse;
font-size:14px;
}

th,td{
padding:5px;
border-bottom:1px solid rgba(255,255,255,0.2);
}

tr:hover{
background:rgba(255,255,255,0.1);
}

</style>
</head>

<body>

<h1>Rubik Timer</h1>

<div id="scramble"></div>

<div id="timer">0.000</div>

<div id="stats">
PB: <span id="pb">-</span> |
AO5: <span id="ao5">-</span>
</div>

<button onclick="clearTimes()">Usuń czasy</button>

<div id="timesBox">

<h3>Czasy</h3>

<table>
<thead>
<tr>
<th>#</th>
<th>Czas</th>
</tr>
</thead>

<tbody id="timesTable"></tbody>

</table>

</div>

<script>

let timer=document.getElementById("timer")
let scrambleText=document.getElementById("scramble")
let table=document.getElementById("timesTable")

let running=false
let ready=false
let startTime
let interval

let times=JSON.parse(localStorage.getItem("rubikTimes"))||[]

const moves=["R","L","U","D","F","B"]
const mods=["","'","2"]

function newScramble(){

let scramble=[]

for(let i=0;i<20;i++){

let move=moves[Math.floor(Math.random()*moves.length)]
let mod=mods[Math.floor(Math.random()*mods.length)]

scramble.push(move+mod)

}

scrambleText.innerText=scramble.join(" ")

}

function updateTimer(){

let time=(Date.now()-startTime)/1000
timer.innerText=time.toFixed(3)

}

function saveTimes(){
localStorage.setItem("rubikTimes",JSON.stringify(times))
}

function showTimes(){

table.innerHTML=""

times.forEach((t,i)=>{

let row=document.createElement("tr")

row.innerHTML=`
<td>${i+1}</td>
<td>${t.toFixed(3)}</td>
`

table.appendChild(row)

})

}

function calculatePB(){

if(times.length===0)return

let best=Math.min(...times)

document.getElementById("pb").innerText=best.toFixed(3)

}

function calculateAO5(){

if(times.length<5)return

let last5=times.slice(-5)

let max=Math.max(...last5)
let min=Math.min(...last5)

let filtered=last5.filter(t=>t!==max && t!==min)

let avg=filtered.reduce((a,b)=>a+b)/filtered.length

document.getElementById("ao5").innerText=avg.toFixed(3)

}

function clearTimes(){

if(confirm("Usunąć wszystkie czasy?")){

times=[]
saveTimes()
showTimes()

document.getElementById("pb").innerText="-"
document.getElementById("ao5").innerText="-"

}

}

document.addEventListener("keydown",e=>{

if(e.code==="Space" && !running){

timer.classList.add("ready")
ready=true

}

})

document.addEventListener("keyup",e=>{

if(e.code==="Space"){

if(!running && ready){

timer.classList.remove("ready")

running=true
ready=false

startTime=Date.now()

interval=setInterval(updateTimer,10)

}

else if(running){

clearInterval(interval)

running=false

let final=(Date.now()-startTime)/1000

times.push(final)

saveTimes()
showTimes()

calculatePB()
calculateAO5()

newScramble()

timer.innerText=final.toFixed(3)

}

}

})

newScramble()
showTimes()
calculatePB()
calculateAO5()

</script>

</body>
</html>
