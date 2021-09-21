<template>
  <div>
    <h1>Mi primer componente</h1>
    <!-------Interpolación----->
    <h2>{{subtitulo}}</h2>
    <!---crear boton para llamar metodo--->
    <button @click="sumar">Sumar</button> 
  </div>
</template>

<script>
export default {
    /*datos que manipulan el componente (variables globales)*/
    data: ()=> {
        return {
            subtitulo: 'Calculadora'
        }
    },
    methods: {
        sumar(){
            console.log("metodo sumar")
        }
    },
    created : ()=>{
        console.log("Calculadora creada")
    }
};
</script>

<style>
</style>