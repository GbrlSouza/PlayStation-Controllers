<template>
  <div class="controle">
    <!-- Gatilhos -->
    <div class="gatilho gatilho-esquerdo"></div>
    <div class="gatilho gatilho-direito"></div>

    <!-- Corpo principal -->
    <div class="corpo">
      <!-- Nome "SONY" -->
      <div class="nome">SONY</div>

      <!-- Botões Start e Select -->
      <div class="botao start">Start</div>
      <div class="botao select">Select</div>

      <!-- Botão PS -->
      <div class="botao-ps"></div>

      <!-- Analógicos -->
      <div class="analogico esquerdo"></div>
      <div class="analogico direito"></div>

      <!-- Botões principais -->
      <div class="botoes-principais">
        <Botao label="Δ" color="#2ecc71" />
        <Botao label="◯" color="#e74c3c" />
        <Botao label="✖" color="#3498db" />
        <Botao label="□" color="#f1c40f" />
      </div>

      <!-- Botões direcionais -->
      <div class="botoes-direcionais">
        <Botao label="▲" />
        <Botao label="◄" />
        <Botao label="▼" />
        <Botao label="►" />
      </div>
    </div>
  </div>
</template>

<script>
import Botao from './Botao.vue';

export default {
  components: {
    Botao,
  },
};
</script>

<style scoped>
/* Estilo principal do controle */
.controle {
  position: relative;
  width: 500px;
  height: 320px;
  background: #f5f5f5;
  border-radius: 20px;
  box-shadow: inset -5px -5px 15px rgba(0, 0, 0, 0.1), inset 5px 5px 15px rgba(255, 255, 255, 0.5);
}

/* Gatilhos superiores */
.gatilho {
  position: absolute;
  width: 100px;
  height: 30px;
  background: #e1e1e1;
  border-radius: 20px;
  top: -20px;
}

.gatilho-esquerdo {
  left: 60px;
}

.gatilho-direito {
  right: 60px;
}

/* Corpo principal */
.corpo {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  flex-direction: column;
}

/* Nome SONY */
.nome {
  position: absolute;
  top: 15px;
  font-family: 'Arial', sans-serif;
  font-size: 22px;
  font-weight: bold;
  color: #555;
}

/* Botões Start e Select */
.botao.start,
.botao.select {
  position: absolute;
  top: 50px;
  width: 90px;
  height: 35px;
  background: #d1d1d1;
  border-radius: 12px;
  text-align: center;
  line-height: 35px;
  font-size: 16px;
  color: #333;
  font-weight: bold;
}

.botao.start {
  right: 130px;
}

.botao.select {
  left: 130px;
}

/* Botão PS */
.botao-ps {
  position: absolute;
  bottom: 45px;
  left: 50%;
  transform: translateX(-50%);
  width: 55px;
  height: 55px;
  background: radial-gradient(circle, #000, #444);
  border-radius: 50%;
}

/* Analógicos */
.analogico {
  position: absolute;
  width: 80px;
  height: 80px;
  background: radial-gradient(circle, #333, #000);
  border-radius: 50%;
  border: 4px solid #222;
}

.analogico.esquerdo {
  bottom: 80px;
  left: 100px;
}

.analogico.direito {
  bottom: 80px;
  right: 100px;
}

/* Botões principais */
.botoes-principais {
  position: absolute;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
  top: 130px;
}

.botoes-direcionais {
  position: absolute;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
  left: 50px;
  top: 130px;
}

/* Botões direcionais */
.botoes-direcionais .botao {
  font-size: 20px;
  font-weight: bold;
  color: #333;
  text-align: center;
  width: 40px;
  height: 40px;
  border-radius: 8px;
  background: #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: background-color 0.2s ease;
}

.botoes-direcionais .botao:hover {
  background-color: #aaa;
}
</style>
