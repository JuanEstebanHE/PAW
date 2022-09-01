<template>
    <h2>Cantidad de estudiantes</h2>
    <input type="number" v-model="total" />
    <div v-for="(estudiante,indx) in estudiantes" :key="indx">
        <h2>Ingrese nombre del estudiante {{indx+1}}</h2>
        <input type="text" v-model="estudiante.nombre"/>
        <h2> Ingrese notas del estudiante {{indx+1}}</h2>
        <div>Primera nota: <input type="number" v-model="estudiante.nota1"/> Segunda nota: <input type="number" v-model="estudiante.nota2"/> Tercera nota: <input type="number" v-model="estudiante.nota3"/></div>
        <h2> Resultado</h2>
        <h3>El estudiante {{estudiante.nombre}} numero {{indx+1}} {{(estudiante.nota1+estudiante.nota2+estudiante.nota3)/3>3?'Pasa la materia':"No pasa la materia"}}</h3>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                total:0
            }
        },
        computed:{
            estudiantes(){
                let es = [];
                for(let i = 0;i <this.total;i++){
                    es.push({estudiante:{
                    nombre:"",
                    nota1:0,
                    nota2:0,
                    nota3:0}})
                }
                return es;
            }
        }
    }
</script>