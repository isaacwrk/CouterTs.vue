<template>
<div>
<h1>Contador</h1>
<h2>{{valor}}</h2>
</div>
</template>

<script lang='ts'>
import { defineComponent } from 'vue';

const contador = defineComponent({
    data(){
        return{
            valor:0
        }
    },
    methods:{
        setValor(delta:number){
            this.valor += delta
        }
    }
});
export default contador;

</script>

<style>

</style>