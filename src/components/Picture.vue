<template>
<!-- // Conceitos abordados: Argumentos dinâmicos -->
    <img :src="avatar" :alt="descricao">
</template>
<script>
export default{
    name: 'Picture',
    data(){
        return{
            avatar: "/img/avatar.png",
            descricao: 'Vag profile picture'
        }
    }
}
</script>