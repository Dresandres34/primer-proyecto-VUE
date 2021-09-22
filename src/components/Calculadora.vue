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
    <br>
    <br>
    <!---crear boton para llamar metodo sumar --->
    <button @click="sumar(numero_1, numero_2,numero_3)">Sumar</button>
    <br>
    <br>
    <!---crear boton para llamar metodo multiplicar--->
    <button @click="multiplicar">Multiplicar</button>
    <br>
    <br>
    <!---crear boton para llamar metodo multiplicar--->
    <button @click="dividir">Dividir</button>
    <br>
    <br>
    <span id="resultado">Resultado: {{resultado}}</span>
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
            numero_3: null,
            resultado: ''
        }
    },
    methods: {
        sumar(numero_1, numero_2, numero_3){
            console.log("metodo sumar");
            //sin casteo concatena los valores como string
            console.log("Concatena: ",(numero_1+numero_2+numero_3));
            // sumar valores
            this.resultado = parseInt(numero_1)+parseInt(numero_2)+parseInt(numero_3);
        },
        // Realizar el metodo de multiplciar sin recibir para metros 
        multiplicar (){
            console.log("metodo Multiplicar");
            this.resultado = parseFloat(this.numero_1)* parseFloat(this.numero_2)* parseFloat(this.numero_3);
        },
        //realizar metodo dividir, vierificando que el numero_2 no sea 0
        dividir (){
            console.log("metodo dividir");
            if (parseFloat(this.numero_2)>0) {
                this.resultado = parseFloat (this.numero_1)/ parseFloat(this.numero_2) 
            } else {
                alert("No es posible realizar la división")
            };
        }
    },
    created : ()=>{
        console.log("Calculadora creada")
    }
};
</script>

<style>
</style>