<template>
  <div>
    <h1>Mi primer componente</h1>
    <!-------Interpolación----->
    <h2>{{subtitulo}}</h2>
    <!---crear imput para enviar parametros al metodo sumar---> 
    <input type="number" id="num1" placeholder="Numero 1" v-model="numero_1"/>
    <br>
    <br>
    <input type="number" id="num2" placeholder="Numero 2" v-model="numero_2"/>
    <br>
    <br>
    <input type="number" id="num3" placeholder="Numero 3" v-model="numero_3"/>
    <br>
    <!---crear boton para llamar metodo--->
    <!--button @click="">Sumar</button>---->
  </div>
</template>

<script>
export default {
    /*datos que manipulan el componente (variables globales)*/
    data: ()=> {
        return {
            subtitulo: 'Calculadora',
            numero_1: null,
            numero_2: null,
            numero_3: null
        }
    },
    methods: {
        sumar(numero_1, numero_2, numero_3){
            console.log("metodo sumar")
            console.log("Resultado: ",(numero_1+numero_2+numero_3))
        }
    },
    created : ()=>{
        console.log("Calculadora creada")
    }
};
</script>

<style>
</style>