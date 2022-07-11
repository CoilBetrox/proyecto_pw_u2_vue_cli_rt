<template>
    <!-- HTML -->
    <h2>Contador!</h2>
    <p>{{numero}} <sup>2</sup> = {{obtenerCuadradoComputado}} </p>
    <p>{{numero}} <sup>2</sup> = {{obtenerCuadradoComputado}} </p>
    <p>{{numero}} <sup>2</sup> = {{obtenerCuadradoComputado}} </p>
    <p>{{numero}} <sup>2</sup> = {{obtenerCuadradoComputado}} </p>
    <p>{{numero}} <sup>2</sup> = {{obtenerCuadradoComputado}} </p>
    
    <div>
        <button v-on:click="incrementar">+1</button>
        <button v-on:click="decrementar">-1</button>
    </div>

    <div class="calcula">
        <div class="titCal">
            <p class="calc">Calculadora</p>
        </div>
        <div class="num">
            <div>
                <label for="" class="labl">Num 1: </label>
                <input type="number" v-model="numero1">
            </div>

            <div>
                <label for="" class="labl">Num 2: </label>
                <input type="number" v-model="numero2">                
            </div>
        </div>

        <div class="oper">
            <button class="bt" v-on:click="sumar">+</button>
            <button class="bt" v-on:click="restar">-</button>
            <button class="bt" v-on:click="multi">*</button>
            <button class="bt" v-on:click="divi">/</button>
        </div>

        <div class="resu">
            <p class="resul">Resultado: {{result}}</p>
        </div>
    </div>

</template>

<script>
export default {
    // no olvidarse this
    name: "Contador123",
    data () {
        return{
            numero:5,
            numero1: '',
            numero2: '',
            result:0
        }
    },
    methods:{
        obtenerCuadrado(){
            console.log('Entro al calculo cuadrado')
            return this.numero * this.numero
        },
        incrementar(){
            return this.numero++
        },
        decrementar(){
            return this.numero--
        },
        sumar(){
            console.log('Entro al calculo cuadrado')
            this.result = this.numero1 + this.numero2
            return this.result
        },
        restar(){
            console.log('Entro al calculo cuadrado')
            this.result = this.numero1 - this.numero2
            return this.result
        },
        multi(){
            console.log('Entro al calculo cuadrado')
            this.result = this.numero1 * this.numero2
            return this.result
        },
        divi(){
            console.log('Entro al calculo cuadrado')
            this.result = this.numero1 / this.numero2
            return this.result
        }
    },
    computed:{
        obtenerCuadradoComputado(){
            console.log('Entro cuadrado computado')
            return this.numero * this.numero
        }
    }
}
</script>

<style>

button{
    background-color: rgb(4, 151, 95);
    color: rgb(87, 0, 82);
    border-radius: 5px;
    margin: 0 5px;
    cursor: pointer;
}

button:hover{
    background-color: rgb(87, 0, 82);
    color: rgb(4, 151, 95);
    transition: 0.1s ease-in-out;
}

input{
    margin-bottom: 10px;
}

.calcula{
    display: grid;
    grid-template-columns: 1fr;
}

.titCal{
    margin-top: 1em;
}

.bt{
    background-color: black;
    color: white;
}

.bt:hover{
    background-color: white;
    color: black;
}

.calc{
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-weight: bold;
}

.labl, .resul{
    font-family: 'Courier New', Courier, monospace;
}

</style>