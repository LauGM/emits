<template>
  <div id="app">
    <div class="row m-2">
      <h2>Frases</h2>
      <CardFrase v-for="(frase,index) of frases" :key="index" :frase="frase"/>
    </div>
    <NuevaFrase @recibirFrase="frases.push($event)"/>
    <hr>
    <SlotHijo>
      <img src="./assets/logo.png" alt="logo">
      <p slot="pie">whatsApp: {{ celular }}</p>
    </SlotHijo>
    <hr>
    <FiltrosPrecios />
  </div>
</template>

<script>
import CardFrase from './components/CardFrase.vue';
import FiltrosPrecios from './components/FiltrosPrecios.vue';
import NuevaFrase from './components/NuevaFrase.vue';
import SlotHijo from './components/SlotHijo.vue';

export default {
  name: 'App',
  components: {
    CardFrase,
    NuevaFrase,
    SlotHijo,
    FiltrosPrecios
},
  data() {
    return {
      frases: ['Persevera y triunfaras','Haz bien sin mirar a quien'],
      celular: '1123457878'
    };
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

/* .cartas{
  display: flex;
  flex-direction: row;
} */
</style>
