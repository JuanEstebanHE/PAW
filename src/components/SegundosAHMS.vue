<template>
    <h2>Conversor de segundos a Horas:Minutos:Segundos</h2>
    <h3>Segundos dados</h3>
    <p>{{segundos}}</p>
    <h3>Conversion</h3>
    <p>hh:mm:ss = {{Math.floor(segundos/3600)}}:{{Math.floor((segundos%3600)/60)}}:{{segundos%60}}</p>
</template>

<script>
    export default{
        name:"SegundosAHMS",
        props:{
            segundos: Number
        }
    }
</script>

<style scoped>
</style>