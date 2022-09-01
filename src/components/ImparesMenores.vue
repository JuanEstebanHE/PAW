<template>
    <h2>Ingrese un número</h2>
    <input type="number" v-model="numero"/>
    <h2>Números impares menores</h2>
    <div v-for="n in numeros" :key="n">
        {{n}}
    </div>
</template>

<script>
    export default {
        data(){
            return {
                numero:0
            }
        },
        computed:{
            numeros(){
                let x = [];
                for(let i = 1; i<this.numero; i+=2){
                    x.push(i)
                }
                return x
            }
        }
    }
</script>