<template>
  <div id="app">
    <Contador/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Contador from '@/components/Contador.vue'

@Options({
  components: {Contador},
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ccbfbf;
  margin-top: 10px;
}

</style>
