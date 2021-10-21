<template>
<div>
    <h1>Contador</h1>
    <h2>{{ valor }}</h2>
    <button @click="setValor(-1)">Dec</button>
    <button @click="setValor(1)">Inc</button>
</div>
</template>

<script lang='ts'>
import { defineComponent } from 'vue';

const contador = defineComponent({
    props:{
        valorInicial:{
            type:Number
        }
    },
    data(){
        return{
            valor: this.valorInicial 
        }
    },
    methods:{
        setValor(delta:number):any{
            this.valor! += delta
        }
    }
});
export default contador;
</script>

<style>

</style>