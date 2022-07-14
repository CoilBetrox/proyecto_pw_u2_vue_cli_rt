<template>
    <h2></h2>
    <label for="">Nombre {{ nombre }}</label>
    <input type="text">
    
    <label for="">Apellido {{ apellido }}</label>
    <input type="text">

    <label for="">Correo {{ correo }}</label>
    <input type="text">
    
</template>

<script>
export default {
    props:{
        tipo:String,
        nombre:String,
        apellido:String,
        correo:String
    },
    data(){
        return{
            
        }
    },
    methods:{

    },
    computed:{

    }

}
</script>

<style>

label{
    display: block;
}

</style>