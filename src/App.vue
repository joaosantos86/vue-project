<script setup>
import { ref, onMounted } from 'vue' // importa uma função do vue

const contador = ref(0) // da um valor a alguma variavel

function incrementarContador() {
  contador.value++
}
function decrementarContador(){
  if (contador.value > 0)
  contador.value--
}

function resetarContador() {
  contador.value = 0
}

onMounted (() => {
  console.log("O valor inicial do contador é " + contador.value)
})

</script>

<template>
<button @click="incrementarContador">Incrementar</button>
<button @click="decrementarContador">Decrementar</button>
<button @click="resetarContador">Reiniciar</button>
<p> O valor do contador é: {{ contador }}</p>
</template>

<style scoped>

button {
  font-weight: bold;
}
</style>
