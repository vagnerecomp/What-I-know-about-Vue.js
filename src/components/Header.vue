<template>
    <!-- CSS scoped vs global -->
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Projetos</a></li>
        <li><a href="#">Contato</a></li>
        <li v-if="esta_logado"><a href="#">Mostrar Perfil</a></li> <!-- usando a prop "esta_logado, que é um dado que vem do componente App.vue-->
    </ul>
</template>

<script>
export default {
    name: 'Header',
    props: ["esta_logado"] //declarando a prop "esta_logado" em um array chamado prop
}
</script>

<style scoped>
    ul{
        list-style: none;
        display: flex;
        background-color: #343434;
    }
    li{
        margin-right: 10px;
    }
    a{
        color: #ddd;
        text-decoration: none;
        transition: 5s;
    }
    a:hover{
        color: turquoise;
    }
</style>