<template>
    <!-- conceitos: Componentização -->
    
    <div>
        <h2>Meu formulário</h2>
        <form action="">
            <fieldset>
                <legend style="margin: auto;">Cadastro de Usuários</legend>
                <div><InputText/></div>
                <div><InputText/></div>
                <div><Submit/></div>

            </fieldset>
        </form>
    </div>
</template>
<script>
import InputText from './Form/InputText.vue'
import Submit from './Form/Submit.vue'
export default {
    name: 'Form',
    components:{
        InputText,
        Submit
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