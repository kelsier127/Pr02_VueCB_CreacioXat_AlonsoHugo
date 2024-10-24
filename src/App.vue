<script setup>
import { reactive } from 'vue';
import MissatgeComponent from './components/MissatgeComponent.vue'

let messageArray = reactive([])

function recibir(missatge) {
  console.log(missatge)

  
  messageArray.push(missatge)

  console.log(messageArray)
}
</script>

<template>
  <div>
    <MissatgeComponent @enviar="recibir" />
  </div>
</template>

<style scoped></style>
