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
    <div class="aplicacion">
      <ul0>
        <li v-for="(message, index) in messageArray" :key="index">
          <span>User 1:</span>
          <p> {{ message }} </p>
        </li>
      </ul0>
    </div>
    
    <MissatgeComponent class="pep" @enviar="recibir" />
  </div>
</template>

<style scoped>
ul {
  margin: 0;
  padding: 0;
  list-style-type: none;  /* Elimina las viñetas o puntos de la lista */
  background: none;      /* Elimina cualquier fondo predeterminado */
  border: none;          /* Elimina cualquier borde */
}

span{
  font-weight: bold;
}

.pep{
  position: relative;
}

li{
  list-style-type: none;
  background-color: rgba(88, 163, 228, 0.527);
  padding:15px;
  border-radius:8px;
  justify-content: center;
  margin:10px
}

.aplicacion{
  background-color: rgb(117, 117, 207);
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 700px;
  overflow: auto;
  border-radius:10px
}

</style>
