
<script setup>
    import { ref } from 'vue';

    const emit = defineEmits(['enviar'])

    let missatge = ref("")
    function enviar(){
        
        emit("enviar",missatge.value)
    }
</script>

<template>
    <div>
        <input placeholder="Escribe tu mensaje tet" v-model="missatge">
        <button @click="enviar">Enviar mensaje</button>
    </div>
</template>

<style scoped>

</style>
