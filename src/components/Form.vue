<template>
    <!-- conceitos: Componentização,eventos em Vue.js -->
    
    <div>
        <h2>Meu formulário</h2>
        <form action="" @submit ="enviarFormulario($event)">
            <fieldset>
                <legend style="margin: auto;">Cadastro de Usuários</legend>
                <div>
                    <input type="" v-model="name">
                </div>
                <div>
                    <input type="email" v-model="email">
                </div>
                <div><Submit/></div>

            </fieldset>
        </form>
    </div>
</template>
<script>
// import InputText from './Form/InputText.vue'
import Submit from './Form/Submit.vue'
export default {
    name: 'Form',
    data(){
        return{
            name: "",
            email: ""
        }
    },
    components:{
        // InputText,
        Submit
    },
    methods: {
        enviarFormulario(e){
            e.preventDefault()

            const name = this.name
            const email = this.email
            alert(`O nome é: ${name} e o email é: ${email}`)

            // O próximo passo seria uma requisição Ajax assíncrona para o servidor
            // E inserir os dados no banco
        }
    }
}
</script>
<style scoped>
    form{
        width: 400px;
        display: flex;
        padding: 0;
    }
</style>