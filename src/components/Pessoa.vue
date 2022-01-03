<template>
    <!-- Conceitos abordados: Componentização, dados dinâmicos -->
    <div>
        <h2>Descrição da pessoa: {{nome}}</h2> 
        <Info :compEmail= "compEmail"/> <!-- passando propriedades de componente pai para componente filho com props -->
        <Form />
    </div>
</template>

<script>
import Info from './Info.vue'
import Form from './Form.vue'
export default {
    name: 'Pessoa',  
    components:{
        Info,
        Form
    },   
    data() {
        return{
            nome: 'Vag',
            compEmail: 'vag@binance.com'
        }
    }
}
</script>