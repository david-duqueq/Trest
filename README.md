<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>App Simulador</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<!-- INPUTS ESCONDIDOS PARA UPLOAD -->
<input type="file" id="inputPerfil" accept="image/*" hidden>
<input type="file" id="inputCirculos1" accept="image/*" hidden>
<input type="file" id="inputCirculos2" accept="image/*" hidden>
<input type="file" id="inputCirculos3" accept="image/*" hidden>
<input type="file" id="inputCirculos4" accept="image/*" hidden>
<input type="file" id="inputCirculos5" accept="image/*" hidden>
<input type="file" id="inputCirculos6" accept="image/*" hidden>
<input type="file" id="inputCirculos7" accept="image/*" hidden>
<input type="file" id="inputCirculos8" accept="image/*" hidden>
<input type="file" id="inputCirculos9" accept="image/*" hidden>

<!-- MENU LATERAL ESQUERDO -->
<aside id="menuLateralEsq">
    <h3>Configurações</h3>

    <button onclick="abrirUploadPerfil()">Mudar foto do perfil</button>
    <button onclick="abrirMenuCirculos()">Mudar foto dos 9 círculos</button>

    <!-- Menu para selecionar cada círculo individualmente -->
    <div id="menuCirculos" class="menuCirculos">
        <p>Escolha o círculo para mudar:</p>
        <div class="grid-circulos">
            <button onclick="abrirUploadCirculo(1)">1</button>
            <button onclick="abrirUploadCirculo(2)">2</button>
            <button onclick="abrirUploadCirculo(3)">3</button>
            <button onclick="abrirUploadCirculo(4)">4</button>
            <button onclick="abrirUploadCirculo(5)">5</button>
            <button onclick="abrirUploadCirculo(6)">6</button>
            <button onclick="abrirUploadCirculo(7)">7</button>
            <button onclick="abrirUploadCirculo(8)">8</button>
            <button onclick="abrirUploadCirculo(9)">9</button>
        </div>
    </div>
</aside>

<!-- MENU LATERAL DIREITO -->
<aside id="menuLateralDir">
    <h3>Ajuda</h3>
    <p>para ter acesso ao aplicativo entre em contato</p>
    <a href="#">Clique aqui para mais info</a>
</aside>

<!-- OVERLAY -->
<div id="overlay" onclick="fecharMenus()"></div>

<!-- HEADER -->
<header class="header">
    <div class="status-bar">
        <div class="perfil" onclick="abrirMenuEsq()">
            <img id="fotoPerfil" src="https://via.placeholder.com/40">
        </div>

        <div class="interrogacao" onclick="abrirMenuDir()">?</div>
    </div>
</header>

<!-- CONTEÚDO -->
<main class="content">

    <!-- CONTA -->
    <section class="bloco">
        <p class="label">Conta</p>
        <h1>R$ 97.518,38</h1>
    </section>

    <!-- MENU CIRCULAR -->
    <section class="menu">
        <div class="menu-scroll">

            <!-- 9 CÍRCULOS -->
            <div class="menu-item"><div class="circle"><img class="icone"></div><p>Área Pix</p></div>
            <div class="menu-item"><div class="circle"><img class="icone"></div><p>Pagar</p></div>
            <div class="menu-item"><div class="circle roxo"><img class="icone"></div><p>Pegar<br>emprestado</p></div>
            <div class="menu-item"><div class="circle"><img class="icone"></div><p>Transferir</p></div>
            <div class="menu-item"><div class="circle"><img class="icone"></div><p>Recarga</p></div>
            <div class="menu-item"><div class="circle"><img class="icone"></div><p>Cartões</p></div>
            <div class="menu-item"><div class="circle"><img class="icone"></div><p>Investir</p></div>
            <div class="menu-item"><div class="circle"><img class="icone"></div><p>Seguro</p></div>
            <div class="menu-item"><div class="circle"><img class="icone"></div><p>Ajuda</p></div>

        </div>
    </section>

    <!-- CARDS -->
    <section class="card destaque-card"><p>Pix no Crédito</p><span>Transfira sem usar o saldo da conta.</span></section>
    <section class="card"><p class="label">Cartão de crédito</p><h2>R$ 16,44</h2><span>Limite disponível de R$ 983,56</span></section>
    <section class="card"><p class="label">Empréstimo</p><span>Valor disponível de até</span><h2>R$ 50.000,00</h2></section>

</main>

<script src="script.js"></script>

        <!-- css -->
        <Style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  background: #000;
  color: #fff;
}

/* HEADER */
.header {
  background: #6a1b9a;
  padding: 2vw;
}

.status-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.perfil img {
  width: 10vw;
  max-width: 50px;
  height: 10vw;
  max-height: 50px;
  border-radius: 50%;
  border: 2px solid #fff;
  cursor: pointer;
}

.interrogacao {
  width: 8vw;
  max-width: 40px;
  height: 8vw;
  max-height: 40px;
  border-radius: 50%;
  background: #fff;
  color: #000;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  font-weight: bold;
  font-size: clamp(14px, 2vw, 18px);
}

/* CONTEÚDO */
.content {
  padding: 4vw;
}

.bloco {
  margin-bottom: 4vw;
}

.label {
  color: #aaa;
  font-size: clamp(12px, 2vw, 16px);
}

h1 {
  font-size: clamp(20px, 5vw, 28px);
  margin-top: 2vw;
}

/* MENU CIRCULAR */
.menu {
  margin-bottom: 4vw;
}

.menu-scroll {
  display: flex;
  gap: 4vw;
  overflow-x: auto;
}

.menu-scroll::-webkit-scrollbar {
  display: none;
}

.menu-item {
  min-width: 18vw;
  text-align: center;
}

.circle {
  width: 18vw;
  max-width: 64px;
  height: 18vw;
  max-height: 64px;
  background: #1c1c1c;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.circle.roxo {
  background: #6a1b9a;
}

.icone {
  width: 8vw;
  max-width: 30px;
  height: 8vw;
  max-height: 30px;
  border-radius: 50%;
}

.menu-item p {
  margin-top: 1vw;
  font-size: clamp(10px, 2vw, 14px);
  color: #ccc;
}

/* CARDS */
.card {
  background: #141414;
  border-radius: 4vw;
  padding: 4vw;
  margin-bottom: 4vw;
}

.card span {
  color: #999;
  font-size: clamp(12px, 2vw, 14px);
}

.card h2 {
  margin-top: 1vw;
  font-size: clamp(16px, 4vw, 22px);
}

.destaque-card {
  background: #1b1b1b;
}

/* MENU LATERAL */
#menuLateralEsq,
#menuLateralDir {
  position: fixed;
  top: 0;
  height: 100%;
  width: 70vw;
  max-width: 300px;
  background: #111;
  padding: 4vw;
  transition: 0.3s;
  z-index: 10;
}

#menuLateralEsq { left: -100%; }
#menuLateralDir { right: -100%; }

#menuLateralEsq button,
#menuLateralDir button {
  width: 100%;
  padding: 2vw;
  margin-top: 2vw;
  background: #6a1b9a;
  color: #fff;
  border: none;
  border-radius: 2vw;
}

/* MENU CÍRCULOS */
.menuCirculos {
  display: none;
  margin-top: 2vw;
}

.grid-circulos {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2vw;
  margin-top: 2vw;
}

.grid-circulos button {
  padding: 2vw;
  background: #6a1b9a;
  color: #fff;
  border: none;
  border-radius: 1vw;
  cursor: pointer;
}

/* OVERLAY */
#overlay {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.6);
  z-index: 5;
}
        </Style>
        
        <!-- java -->
        
        
        <script>
            // ELEMENTOS
const fotoPerfil=document.getElementById("fotoPerfil")
const inputPerfil=document.getElementById("inputPerfil")
const overlay=document.getElementById("overlay")
const menuEsq=document.getElementById("menuLateralEsq")
const menuDir=document.getElementById("menuLateralDir")
const menuCirculos=document.getElementById("menuCirculos")
const icones=document.querySelectorAll(".icone")
const inputsCirculos=[null,document.getElementById("inputCirculos1"),document.getElementById("inputCirculos2"),document.getElementById("inputCirculos3"),document.getElementById("inputCirculos4"),document.getElementById("inputCirculos5"),document.getElementById("inputCirculos6"),document.getElementById("inputCirculos7"),document.getElementById("inputCirculos8"),document.getElementById("inputCirculos9")]

// ABRIR MENU ESQUERDO
function abrirMenuEsq(){menuEsq.style.left="0";overlay.style.display="block"}
// ABRIR MENU DIREITO
function abrirMenuDir(){menuDir.style.right="0";overlay.style.display="block"}
// FECHAR TODOS
function fecharMenus(){menuEsq.style.left="-260px";menuDir.style.right="-260px";menuCirculos.style.display="none";overlay.style.display="none"}

// UPLOAD FOTO PERFIL
function abrirUploadPerfil(){inputPerfil.click()}
inputPerfil.addEventListener("change",()=>{const file=inputPerfil.files[0];const reader=new FileReader();reader.onload=()=>{fotoPerfil.src=reader.result;localStorage.setItem("fotoPerfil",reader.result)};reader.readAsDataURL(file);fecharMenus()})

// MOSTRAR MENU PARA ESCOLHER CÍRCULOS
function abrirMenuCirculos(){menuCirculos.style.display="block"}

// ABRIR UPLOAD CÍRCULO INDIVIDUAL
function abrirUploadCirculo(n){inputsCirculos[n].click()}
inputsCirculos.forEach((input,i)=>{if(i>0)input.addEventListener("change",()=>{const file=input.files[0];const reader=new FileReader();reader.onload=()=>{icones[i-1].src=reader.result;localStorage.setItem("circulo"+i,reader.result)};reader.readAsDataURL(file);fecharMenus()})})

// CARREGAR IMAGENS SALVAS
window.onload=()=>{
    const perfilSalvo=localStorage.getItem("fotoPerfil")
    if(perfilSalvo)fotoPerfil.src=perfilSalvo
    for(let i=1;i<=9;i++){const circuloSalvo=localStorage.getItem("circulo"+i);if(circuloSalvo)icones[i-1].src=circuloSalvo}
}
        </script>
</body>
</html>