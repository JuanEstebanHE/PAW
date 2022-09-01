<template>
    <h2>Agregue 10 salarios</h2>
    <input type="number" v-model="salario" /> <input type="button" value="agregar" @click="agregarLista"/><input type="button" value="limpiar" @click="limpiarLista"/>
    <div>{{lista_salarios}}</div>
    <h2>10 Salarios con aumento del 8%</h2>
    <h3 class="error" v-if="lista_salarios.length<10">Debe agregar más salarios</h3>
    <div v-if="lista_salarios.length===10">{{lista_salarios_aumento}}</div>
</template>

<script>
    export default{
        data(){
            return {
                salario:1000,
                lista_salarios:[]
            }
        },
        computed:{
            lista_salarios_aumento(){
                return this.lista_salarios.map((s)=>s*1.08)
            }
        },
        methods:{
            agregarLista(){
                if(this.lista_salarios.length<10){
                    this.lista_salarios.push(this.salario);
                }
            },
            limpiarLista(){
                this.lista_salarios = [];
            }
        }
    }
</script>

<style scoped>
    .error{
        color:rgb(48, 9, 203);
    }
</style>