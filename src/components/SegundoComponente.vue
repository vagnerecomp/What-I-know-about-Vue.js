<template>
    <!-- Conceitos abordados: Primeiros componentes, reutilização de componentes-->
    <div>
        <Reutilizacao />
        <p><br>Chuuuupa React</p>
        <Reutilizacao />
        <Reutilizacao />
        <p>oi</p>
        <Reutilizacao />
    </div>
</template>
<script>
import Reutilizacao from './Reutilizacao.vue'
export default{
    name: 'SegundoComponente',
    components:{
        Reutilizacao
    }
    
}
</script>
