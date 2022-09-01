<template>
  <h1>1.</h1>
    <input type="number" v-model="d1"/>
    <SegundosAHMS :segundos="d1" />
  <h1>2.</h1>
    <input type="number" v-model="d2"/>
    <TotalLlamada :duracion="d2" />
  <h1>3.</h1>
    <SaludoHora />
  <h1>4.</h1>
    n1: <input type="number" v-model="d4.n1"/>, n2: <input type="number" v-model="d4.n2"/>, n3: <input type="number" v-model="d4.n3"/>
    <CantidadIguales :n1="d4.n1" :n2="d4.n2" :n3="d4.n3"/>
  <h1>5.</h1>
    <AgregarOrdenar />
  <h1>6.</h1>
    <ImparesMenores />
  <h1>7.</h1>
   <SalariosPorcentaje />
  <h1>8.</h1>
    <h2>Lista de números aleatorios</h2>
    <div>{{d8}}</div> <input type="button" value="actualizar" @click="actualizarAleatorios"/>
    <DividirArreglo :arreglo="d8"/>
  <h1>9.</h1>
    <ArregloNM />
  <h1>10.</h1>
    <MatrizSumario :matriz="d10" />
  <h1>11.</h1>
    <NotasEstudiante />
  <h1>12.</h1>
    <NotasArregloEstudiantes />
</template>

<script>
import SegundosAHMS from "./components/SegundosAHMS.vue";
import TotalLlamada from "./components/TotalLlamada.vue";
import SaludoHora from "./components/SaludoHora.vue";
import CantidadIguales from "./components/CantidadIguales.vue";
import AgregarOrdenar from "./components/AgregarOrdenar.vue";
import ImparesMenores from "./components/ImparesMenores.vue";
import SalariosPorcentaje from "./components/SalariosPorcentaje.vue";
import DividirArreglo from "./components/DividirArreglo.vue";
import ArregloNM from "./components/ArregloNM.vue";
import MatrizSumario from "./components/MatrizSumario.vue";
import NotasEstudiante from "./components/NotasEstudiante.vue";
import NotasArregloEstudiantes from "./components/NotasArregloEstudiantes.vue";
export default{
  name:"App",
  data(){
    return {
      d1: 0,
      d2: 0,
      d4:{
        n1:0,
        n2:0,
        n3:0
      },
      d8:[ 706, 219, 186, 678, 341, 598, 438, 751, 332, 207 ],
      d10: [ [1,2,3], [4,5,6],[7,8,9]]
    }
  },
  components:{
    SegundosAHMS,
    TotalLlamada,
    SaludoHora,
    CantidadIguales,
    AgregarOrdenar,
    ImparesMenores,
    SalariosPorcentaje,
    DividirArreglo,
    ArregloNM,
    MatrizSumario,
    NotasEstudiante,
    NotasArregloEstudiantes
  },
  methods:{
    agregar_lista(){
      this.d5.lista.push(this.d5.n);
    },
    actualizarAleatorios(){
      this.d8 = [];
      for(let i = 0; i<10;i++)this.d8.push(Math.floor(Math.random()*1000))
    }
  },
}
</script>

<style>
#app{
  text-align: center;
}

h1{
  color:rgb(208, 13, 13)
}

table{
  margin-left: auto;
  margin-right: auto;
}

table, th, td {
  border: 1px solid black;
}
</style>