<template>
    <h2>Total a pagar por la llamada</h2>
    <h3>Duración de la llamada</h3>
    <p>{{duracion}} minutos</p>
    <h3>Total a pagar</h3>
    <p>{{duracion>3?100+(duracion-3)*50:100}}</p>
</template>

<script>
    export default {
        name:"TotalLlamada",
        props:{
            duracion: Number //en minutos
        },
    }
</script>

<style scoped>
</style>