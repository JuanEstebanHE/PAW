<template>
    <h2>Matriz con numero y suma total</h2>
    <table>
        <tr v-for="(row,index) in matriz" :key="index">
            <td v-for="(value,indexx) in row" :key="index + ','+ indexx" >{{value}}</td>
        </tr>
        <tr>
            <td v-for="(value,index) in totales" :key="index">{{value}}</td>
        </tr>
    </table>
</template>

<script>
    export default {
        props:{
            matriz:Array
        },
        computed:{
            totales(){
                let t = Array(this.matriz[0].length).fill(0);
                console.log(this.matriz)
                for(let i = 0; i<this.matriz.length;i++){
                    for(let j = 0; j<this.matriz[i];j++){
                        console.log(this.matriz[i][j])
                        t[j] += this.matriz[i][j];
                    }
                }
                return t;
            }
        }
    }
</script>