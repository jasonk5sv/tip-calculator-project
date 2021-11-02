<template>
  <TipCalculator />
</template>

<script>
import TipCalculator from './components/calc.vue'


export default {
  name: 'App',
  components: {
    TipCalculator
  }
}
</script>

<style>
#app {
  font-family: 'Space Mono', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-left: auto;
  margin-right: auto;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-content: center;
}

@media (min-width: 375px) {
  .calculator {
    width: 100%;
  }

}
</style>
