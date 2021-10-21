<template>

<div class="counter">
    <div class="main">
        <h1>Contador</h1>
        <h2>{{ counter }}</h2>
    </div>
    <div class="buttons">
        <button @click="decreaseCounter">-</button>
        <button @click="increaseConter">+</button>
    </div>
</div>


</template>

<script lang='ts'>
import { defineComponent, ref } from 'vue';

const contador = defineComponent({
     props:{
        initialValue:{
            type:Number
        }
    },
    
    setup(){
        let counter = ref(0)
        const decreaseCounter = function(){
            counter.value--
        }

        const increaseConter = function(){
            counter.value++
        }

        return{
            counter,
            decreaseCounter,
            increaseConter
        }
    }
});
export default contador;
</script>


<style>
.buttons{}
</style>