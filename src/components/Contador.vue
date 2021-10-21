<template>
<div class="counter">
    <div class="main">
        <h1>Contador</h1>
        <h2>{{ counter }}</h2>
    </div>
    <div class="buttons">
        <button class="bminus" @click="decreaseCounter">-</button>
        <button class="bplus" @click="increaseConter">+</button>
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
.theme{
    display: flex;
    flex-direction: column;
    align-content: flex-end;
    align-items: center;
    margin-bottom: 2px;
    position: inherit;
    background-color: grey;
    color: cornsilk;
    border-radius: 4px;
}
.buttons{
    padding-bottom:5px;
}
.bminus{
    background-color: #f44336;
    color: white;
    text-decoration: none;
    font-size: 30px;
    border: none;
    margin-right: 2px;
    border-radius: 2px;
}
.bminus:hover{
    background-color: #f82c1d;
}
.bplus{
    background-color: #94e215;
    color: white;
    text-decoration: none;
    font-size: 30px;
    border:none;
    border-radius: 2px;
}

.bplus:hover{
    background-color:#9df314 ;
}

.counter{
    border-color: #8d8a8a;
    border-style: solid;
    background-color: #2a282e
}
</style>