<template>
  <!-- Conceitos abordados: Componentização  -->
  <div class="main">
    <PrimeiroComponente/>
   <SegundoComponente/>
   <LifeCycle/>
   <Pessoa/>
  </div>
   
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import SegundoComponente from './components/SegundoComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
export default {
  name: 'app',
  components:{
    PrimeiroComponente,
    SegundoComponente,
    LifeCycle,
    Pessoa
  },
  data(){
    return{
      // texto: 
    }
  }
}
</script>

<style scoped>
  .main{
    background-color: #555;
    height: 100vh;
  }
</style>