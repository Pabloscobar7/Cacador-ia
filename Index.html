<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Caçador IA</title>

<style>
body{
  margin:0;
  font-family:Arial,sans-serif;
  background:#101827;
  color:white;
}
.container{
  max-width:700px;
  margin:auto;
  padding:20px;
}
h1{
  text-align:center;
  margin-bottom:5px;
}
.sub{
  text-align:center;
  color:#aeb8c8;
  margin-bottom:25px;
}
.card{
  background:#182235;
  padding:18px;
  border-radius:15px;
  margin-bottom:18px;
}
label{
  display:block;
  margin-top:12px;
  margin-bottom:6px;
  font-weight:bold;
}
input,select{
  width:100%;
  box-sizing:border-box;
  padding:13px;
  border:0;
  border-radius:9px;
  font-size:16px;
}
button{
  width:100%;
  padding:14px;
  margin-top:18px;
  border:0;
  border-radius:9px;
  font-size:16px;
  font-weight:bold;
  background:#20c77a;
  color:white;
}
.resultado{
  background:#202d44;
  padding:15px;
  border-radius:10px;
  margin-top:15px;
}
.stat{
  display:inline-block;
  width:30%;
  text-align:center;
  padding:8px;
}
.numero{
  font-size:25px;
  font-weight:bold;
}
.item{
  border-bottom:1px solid #33415c;
  padding:12px 0;
}
.small{
  color:#aeb8c8;
  font-size:13px;
}
.danger{
  background:#d9534f;
}
</style>
</head>

<body>

<div class="container">

<h1>🎯 CAÇADOR IA</h1>
<div class="sub">Comparador de previsões</div>

<div class="card">

<label>Jogo</label>
<input id="jogo" placeholder="Ex: Adelaide United vs Tai Po">

<label>Odd</label>
<input id="odd" type="number" step="0.01" placeholder="Ex: 1.50">

<label>Mercado</label>
<select id="mercado">
<option>Vencedor</option>
<option>Empate</option>
<option>Mais de 2.5 gols</option>
<option>Menos de 2.5 gols</option>
<option>Ambas marcam</option>
<option>1º tempo</option>
<option>Outro</option>
</select>

<label>IA / Sistema 1</label>
<input id="ia1" placeholder="Previsão">

<label>IA / Sistema 2</label>
<input id="ia2" placeholder="Previsão">

<label>IA / Sistema 3</label>
<input id="ia3" placeholder="Previsão">

<button onclick="analisar()">ANALISAR CONCORDÂNCIA</button>

<div id="analise"></div>

</div>

<div class="card">

<h2>Resultado real</h2>

<input id="resultado" placeholder="Ex: Adelaide United">

<button onclick="registrar()">REGISTRAR RESULTADO</button>

</div>

<div class="card">

<h2>📊 Histórico</h2>

<div class="resultado">

<div class="stat">
<div class="numero" id="jogos">0</div>
<div class="small">Jogos</div>
</div>

<div class="stat">
<div class="numero" id="acertos">0</div>
<div class="small">Acertos</div>
</div>

<div class="stat">
<div class="numero" id="taxa">0%</div>
<div class="small">Taxa</div>
</div>

</div>

<div id="historico"></div>

<button class="danger" onclick="limpar()">APAGAR HISTÓRICO</button>

</div>

</div>

<script>

let historico =
JSON.parse(localStorage.getItem("cacadorIA") || "[]");

function atualizar(){

document.getElementById("jogos").innerText =
historico.length;

let acertos =
historico.filter(x => x.acertou).length;

document.getElementById("acertos").innerText =
acertos;

let taxa =
historico.length ?
Math.round((acertos / historico.length) * 100) : 0;

document.getElementById("taxa").innerText =
taxa + "%";

let html="";

historico.slice().reverse().forEach(x => {

html += `
<div class="item">
<b>${x.jogo}</b><br>
<span class="small">
Mercado: ${x.mercado}<br>
Previsões: ${x.previsoes.join(" | ")}<br>
Resultado: ${x.resultado}<br>
${x.acertou ? "✅ Acertou" : "❌ Errou"}
</span>
</div>
`;

});

document.getElementById("historico").innerHTML = html;
}

function analisar(){

let jogo =
document.getElementById("jogo").value.trim();

let odd =
document.getElementById("odd").value;

let mercado =
document.getElementById("mercado").value;

let previsoes = [
document.getElementById("ia1").value.trim(),
document.getElementById("ia2").value.trim(),
document.getElementById("ia3").value.trim()
].filter(x => x !== "");

if(!jogo){
alert("Coloque o nome do jogo.");
return;
}

if(previsoes.length < 2){
alert("Coloque pelo menos 2 previsões.");
return;
}

let contagem={};

previsoes.forEach(p=>{
let chave=p.toLowerCase();
contagem[chave]=(contagem[chave]||0)+1;
});

let principal =
Object.keys(contagem)
.sort((a,b)=>contagem[b]-contagem[a])[0];

let votos=contagem[principal];

let concordancia =
Math.round((votos/previsoes.length)*100);

document.getElementById("analise").innerHTML = `
<div class="resultado">

<h3>🔎 Análise</h3>

<p><b>Jogo:</b> ${jogo}</p>
<p><b>Mercado:</b> ${mercado}</p>
<p><b>Odd:</b> ${odd || "-"}</p>

<p>
<b>Previsão mais repetida:</b><br>
${principal}
</p>

<p>
<b>Concordância:</b>
${concordancia}%
</p>

<p>
${votos} de ${previsoes.length}
sistemas indicaram a mesma previsão.
</p>

</div>
`;

}

function registrar(){

let jogo =
document.getElementById("jogo").value.trim();

let resultado =
document.getElementById("resultado").value.trim();

if(!jogo || !resultado){
alert("Coloque o jogo e o resultado real.");
return;
}

let previsoes = [
document.getElementById("ia1").value.trim(),
document.getElementById("ia2").value.trim(),
document.getElementById("ia3").value.trim()
].filter(x=>x!=="");

if(previsoes.length < 2){
alert("Primeiro coloque pelo menos 2 previsões.");
return;
}

let acertou =
previsoes.some(p =>
p.toLowerCase() === resultado.toLowerCase()
);

historico.push({

jogo:jogo,

mercado:
document.getElementById("mercado").value,

previsoes:previsoes,

resultado:resultado,

acertou:acertou

});

localStorage.setItem(
"cacadorIA",
JSON.stringify(historico)
);

atualizar();

alert(
acertou ?
"Resultado registrado: houve previsão igual ao resultado." :
"Resultado registrado: nenhuma previsão foi igual ao resultado."
);

document.getElementById("resultado").value="";

}

function limpar(){

if(confirm("Apagar todo o histórico?")){

historico=[];

localStorage.removeItem("cacadorIA");

atualizar();

}

}

atualizar();

</script>

</body>
</html>
