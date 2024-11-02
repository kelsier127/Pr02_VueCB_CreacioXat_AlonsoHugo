
<script setup>
    import { ref } from 'vue';

    const emit = defineEmits(['enviar'])

    let missatge = ref("")
    function enviar(){
        let input = document.getElementById("inputMensaje")
        input.value = ""
        emit("enviar",missatge.value)
    }
</script>

<template>
    <div>
        <input id="inputMensaje" placeholder="Escribe tu mensaje tet" v-model="missatge">
        <button @click="enviar">Enviar mensaje</button>
    </div>
</template>

<style scoped>

</style>
