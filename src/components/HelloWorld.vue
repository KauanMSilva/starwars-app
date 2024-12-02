<script setup lang="ts">
import { ref } from 'vue'
defineProps<{ msg: string }>()

const count = ref(0)
const mutiply = ref(10)
const botaoCorajoso = document.createElement('button');
botaoCorajoso.textContent = 'SÓ CLIQUE CÊ TIVER CORAGEM MESMO';
document.body.appendChild(botaoCorajoso);

botaoCorajoso.style.position = 'fixed';
botaoCorajoso.style.bottom = '20px';  
botaoCorajoso.style.left = '50%';    
botaoCorajoso.style.transform = 'translateX(-50%)'; 
botaoCorajoso.style.padding = '10px 20px';
botaoCorajoso.style.fontSize = '16px';
botaoCorajoso.style.cursor = 'pointer';
botaoCorajoso.style.backgroundColor = 'green';
botaoCorajoso.style.border = 'bold';
botaoCorajoso.style.color = 'pink';

botaoCorajoso.addEventListener('click', function() {
    alert('Parabéns, Você é corajoso mesmo ZéRuela!');
});

</script>

<template>
  <h1>{{ msg }}</h1>

  <button>...</button>

  <div class="card">
    <button type="button" @click="count++">K&C.Tech {{ mutiply*count }}</button>
    <p>
      
      <code class="cor1">K & C. Tecnologia</code> 
    </p>
  </div>

  <p>
    Todos os Direitos Reservados. <br><br>
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >Portifólio.</a
    >
  </p>
  <p class="dev">
    Desenvolvido por K&C.Tech Copyright © 2024
    <a
      href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support"
      target="_blank"
      >Contato</a
    >.
  </p>
  <p class="read-the-docs">Política de Privacidade</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
  font-weight : bold;
  font-family : monospace;
  
}
.cor1 {
  color: red;
  font-size: 50px;

}

.dev {
  color: blueviolet;
  font-weight : bold;
  font-style: oblique;
  justify-content: space-between;
}
</style>
