<template>
    <!-- HTML -->
    <h2>{{ muestraTitulo }}</h2>
    <p>{{numero}} <sup>2</sup> = {{obtenerCuadradoComputado}} </p>
    <p>{{numero}} <sup>2</sup> = {{obtenerCuadradoComputado}} </p>
    <p>{{numero}} <sup>2</sup> = {{obtenerCuadradoComputado}} </p>
    <p>{{numero}} <sup>2</sup> = {{obtenerCuadradoComputado}} </p>
    <p>{{numero}} <sup>2</sup> = {{obtenerCuadradoComputado}} </p>
    
    <div>
        <button v-on:click="incrementar">+1</button>
        <button v-on:click="decrementar">-1</button>
    </div>


</template>

<script>
export default {
    // no olvidarse this
    name: "Contador123",
    props:{
        titulo:String, 
        inicio:{
            type: Number,
            required: false,
            default: 100,
            validator(value){
                //validation return true or false
                return value>0
            }
        }
    },
    data () {
        return{
            numero: this.inicio
        }
    },
    methods:{
        obtenerCuadrado(){
            console.log('Entro al calculo cuadrado')
            return this.numero * this.numero
        },
        incrementar(){
            //return this.numero++
            return this.numero = this.numero + 1
        },
        decrementar(){
            return this.numero--
        }
    },
    computed:{
        obtenerCuadradoComputado(){
            console.log('Entro cuadrado computado')
            return this.numero * this.numero
        },
        muestraTitulo(){
            return this.titulo || "Titulo Vacío 2";
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



</style>