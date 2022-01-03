<template>
  <!-- Conceitos abordados: Componentização  -->
  <div class="main">
    <Header :esta_logado = !true /> <!-- enviando essa prop para o componente Header-->
    <PrimeiroComponente/>           <!-- caso esta_logado seja true, a opção Mostrar Perfil aparece no header, caso contrario, não aparece.-->
    <SegundoComponente/>
    <LifeCycle/>
    <Pessoa/>
  </div>
   
</template>

<script>
import Header from './components/Header.vue'
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
    Pessoa,
    Header
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