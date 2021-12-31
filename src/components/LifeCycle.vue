<template>
    <!-- Conceitos abordados: Lifecycle hooks -->
    <h1>  {{nome}}</h1>
</template>

<script>
export default {
    name: 'LyfeCycle',
    data(){
        return{
            nome: 'E nessa loucura, de dizer que não te quero'
        }
    },
    methods:{
      metodoNoLifeCycle(){
        console.log("positivo e operante")
      }
    },
  created(){
    setTimeout(()=>{
      this.nome = 'Vou negando as aparências, desfarçando as evidências'
    },2000)

    this.metodoNoLifeCycle()
  },
  mounted(){
      setTimeout(()=>{
          this.nome = 'Mas pra que viver fingindo se eu não posso enganar meu coração...'
      },3000)
      this.metodoNoLifeCycle()
  }
}
</script>

