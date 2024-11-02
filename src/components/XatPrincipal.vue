<script setup>
import { reactive } from 'vue';
import MissatgeComponent from './MissatgeComponent.vue'

let messageArray = reactive([])

function recibir(missatge) {
  console.log(missatge)

  
  messageArray.push(missatge)

  console.log(messageArray)
}
</script>

<template>
  <div>
    <ul>
      <li v-for="(message, index) in messageArray" :key="index">
        User 1: {{ message }}
      </li>
    </ul>
    <MissatgeComponent @enviar="recibir" />
  </div>
</template>

<style scoped></style>
