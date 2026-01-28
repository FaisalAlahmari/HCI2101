<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>XO | لعبة إكس أو</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap');

:root{
  --bg:#0f172a;
  --card:rgba(30,41,59,.75);
  --primary:#38bdf8;
  --secondary:#22c55e;
  --danger:#ef4444;
  --text:#f8fafc;
  --glass:blur(12px);
}

body.light{
  --bg:#f1f5f9;
  --card:rgba(255,255,255,.85);
  --text:#020617;
}

*{
  box-sizing:border-box;
  font-family:"Cairo",sans-serif;
}

body{
  margin:0;
  min-height:100vh;
  background:linear-gradient(135deg,var(--bg),#020617);
  color:var(--text);
  display:flex;
  flex-direction:column;
}

.screen{
  flex:1;
  display:none;
  justify-content:center;
  align-items:center;
  padding:20px;
}

.screen.active{display:flex}

.card{
  background:var(--card);
  backdrop-filter:var(--glass);
  border-radius:20px;
  padding:25px;
  width:100%;
  max-width:420px;
  box-shadow:0 20px 50px rgba(0,0,0,.4);
}

h1,h2{text-align:center}

input,select,button{
  width:100%;
  padding:12px;
  border-radius:12px;
  border:none;
  margin:8px 0;
  font-size:16px;
}

input,select{
  background:transparent;
  border:1px solid #64748b;
  color:var(--text);
}

button{
  background:linear-gradient(135deg,var(--primary),#0ea5e9);
  color:#020617;
  font-weight:700;
  cursor:pointer;
}

button:hover{opacity:.9}

.toggle{
  text-align:center;
  cursor:pointer;
  margin-bottom:10px;
}

.board{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:12px;
}

.cell{
  height:90px;
  background:#020617;
  border-radius:16px;
  display:flex;
  justify-content:center;
  align-items:center;
  font-size:48px;
  cursor:pointer;
  transition:.2s;
}

.cell:hover{transform:scale(1.05)}
.cell.X{color:var(--primary)}
.cell.O{color:var(--secondary)}

.info{text-align:center;margin:10px 0;font-size:18px}

.score{
  display:flex;
  justify-content:space-between;
  margin-bottom:10px;
}

footer{
  background:#020617;
  color:#cbd5f5;
  text-align:center;
  padding:10px;
  font-size:14px;
}
</style>
</head>

<body>

<div class="screen active" id="start">
  <div class="card">
    <h1>🎮 XO الاحترافية</h1>

    <div class="toggle" onclick="toggleTheme()">🌙 / ☀️</div>

    <select id="mode">
      <option value="1">لاعب واحد (ضد الكمبيوتر)</option>
      <option value="2">لاعبان</option>
    </select>

    <input id="p1" placeholder="اسم اللاعب الأول">
    <input id="p2" placeholder="اسم اللاعب الثاني">

    <button onclick="startGame()">ابدأ اللعب</button>
  </div>
</div>

<div class="screen" id="game">
  <div class="card">
    <h2>❌ إكس | ⭕ أو</h2>

    <div class="score">
      <div id="sX">0</div>
      <div id="sO">0</div>
    </div>

    <div class="info" id="status"></div>
    <div class="board" id="board"></div>

    <button onclick="newRound()" style="margin-top:10px">🔄 جولة جديدة</button>
    <button onclick="back()" style="background:var(--danger);margin-top:5px">⬅️ العودة</button>
  </div>
</div>

<footer>
  <div>Student Name: FAISAL ABDULAZIZ FAIZ ALAHMARI (فيصل عبدالعزيز بن فايز الاحمري)</div>
  <div>Student ID: 44610108</div>
  <div>Supervised by: Mohammed Ahmed Jabali</div>
</footer>

<script>
let board, current, players, mode, gameOver=false;
let scoreX=0, scoreO=0;

function toggleTheme(){
  document.body.classList.toggle("light");
}

function startGame(){
  mode=document.getElementById("mode").value;
  players={
    X:document.getElementById("p1").value||"اللاعب 1",
    O:document.getElementById("p2").value||(mode==1?"الكمبيوتر":"اللاعب 2")
  };
  scoreX=scoreO=0;
  startRound();
  document.getElementById("start").classList.remove("active");
  document.getElementById("game").classList.add("active");
}

function startRound(){
  board=Array(9).fill("");
  current="X";
  gameOver=false;
  render();
}

function render(){
  document.getElementById("board").innerHTML="";
  board.forEach((v,i)=>{
    let c=document.createElement("div");
    c.className="cell "+v;
    c.textContent=v;
    c.onclick=()=>play(i);
    document.getElementById("board").appendChild(c);
  });
  document.getElementById("status").textContent="الدور على: "+players[current];
  document.getElementById("sX").textContent="❌ "+players.X+": "+scoreX;
  document.getElementById("sO").textContent="⭕ "+players.O+": "+scoreO;
}

function play(i){
  if(board[i]||gameOver) return;
  board[i]=current;
  if(win()){
    gameOver=true;
    current=="X"?scoreX++:scoreO++;
    document.getElementById("status").textContent="🎉 الفائز: "+players[current];
  }else if(!board.includes("")){
    gameOver=true;
    document.getElementById("status").textContent="🤝 تعادل";
  }else{
    current=current=="X"?"O":"X";
    if(mode==1&&current=="O") setTimeout(ai,500);
  }
  render();
}

function ai(){
  let empty=board.map((v,i)=>v==""?i:null).filter(v=>v!==null);
  play(empty[Math.floor(Math.random()*empty.length)]);
}

function win(){
  const w=[[0,1,2],[3,4,5],[6,7,8],[0,3,6],[1,4,7],[2,5,8],[0,4,8],[2,4,6]];
  return w.some(a=>a.every(i=>board[i]==current));
}

function newRound(){startRound()}
function back(){
  document.getElementById("game").classList.remove("active");
  document.getElementById("start").classList.add("active");
}
</script>

</body>
</html>
