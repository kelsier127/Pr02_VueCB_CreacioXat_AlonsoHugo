
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
    <div class="inputContainer">
        <input class="textInput" id="inputMensaje" placeholder="Escribe tu mensaje tet" v-model="missatge">
        <button class="sendButton" @click="enviar">Enviar mensaje</button>
    </div>
</template>

<style scoped>
.textInput{
    border-radius: 5px;
    height: 40px;
    padding:10px;
    margin: 5px;
}

.sendButton{
    padding:5px;
    background-color: aliceblue;
    border-radius: 4px;
    margin: 5px;
}
.inputContainer{
    display: flex;
    justify-content: center;
    margin-top:10px;
    padding:10px;
    position: sticky;
    bottom: 0;
    background-color: rgb(120, 82, 155);
    border-radius:10px
}
</style>
