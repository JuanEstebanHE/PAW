<template>
    <h2>Ingrese su nombre</h2>
    <input type="text" v-model="estudiante.nombre"/>
    <h2> Ingrese sus notas</h2>
    <div>Primera nota: <input type="number" v-model="estudiante.nota1"/> Segunda nota: <input type="number" v-model="estudiante.nota2"/> Tercera nota: <input type="number" v-model="estudiante.nota3"/></div>
    <h2> Resultado</h2>
    <h3>{{estudiante.nombre}} {{(estudiante.nota1+estudiante.nota2+estudiante.nota3)/3>3?'Pasa la materia':"No pasa la materia"}}</h3>
</template>

<script>
    export default {
        data(){
            return {
                estudiante:{
                    nombre:"",
                    nota1:0,
                    nota2:0,
                    nota3:0
                }
            }
        }
    }
</script>