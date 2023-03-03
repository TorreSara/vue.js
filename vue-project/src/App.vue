<script setup>
import {ref} from 'vue';
//import HelloWorld from './components/HelloWorld.vue'
//import TheWelcome from './components/TheWelcome.vue'
let dato =ref(0);
const sumar= ()=> dato.value++;
const res= ()=> dato.value--;
const restablecer=()=>dato.value=0;


const agregarSeleccionado =()=>{
  if (!seleccionados.value.incluides(dato.value)) {
    seleccionados.value.push(dato.value);
    
  }
};


  

</script>

<template>
<h1 :class="dato >=0?  'positivos' : 'negativo'">{{ dato }}</h1>
<h1>{{ seleccionados }}</h1>
<button @click="sumar">+</button>
<button @click="res">-</button>
<button @click="restablecer">restablecer</button>
<button @click="agregarSeleccionado()">agregar</button>




</template>

<style scoped>
.positivos{
  color: chartreuse;
}
.negativo{
  color: brown;
}
</style>


