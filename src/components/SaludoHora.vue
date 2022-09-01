<template>
    <h2>Saludo</h2>
    <h3>Ingrese su nombre:</h3>
    <input type="text" v-model="nombre"/>
    <h3>Ingrese la hora:</h3>
    <input type="time" v-model="tiempo"/>
    <h3 v-if="saludo && nombre">{{saludo}}, {{nombre}}</h3>
</template>

<script>
    export default{
        name:"SaludoHora",
        data(){
            return {
                nombre:"",
                tiempo:""
            }
        },
        computed:{
            saludo(){
                if(this.tiempo){
                    let hora = Number(this.tiempo.split(":")[0]);
                    if(hora>=0 && hora<12){
                        return "Buenos días";
                    }
                    else if(hora<18){
                        return "Buenas tardes";
                    }
                    else{
                        return "Buenas noches"
                    }
                }
                return ""
            }
        }
    }
</script>

<style scoped>

</style>