<template>
    <div>
        <h2>Nueva frase</h2>
        <input type="text" placeholder="ingresar" v-model="nuevaFrase">
        <button class="btn btn-warning" @click="enviarFrase()">Agregar</button>
    </div>
</template>

<script>
export default {
    name: 'NuevaFrase',

    data() {
        return {
           nuevaFrase:'' 
        };
    },

    methods: {
        enviarFrase(){
            if(this.nuevaFrase){
                this.$emit('recibirFrase',this.nuevaFrase);
                this.nuevaFrase='';
            }
        }
    },
};
</script>

<style scoped>

</style>