<template>
<!-- // Conceitos abordados: Argumentos dinâmicos, emit -->
    <div>
        <img :src="avatar" :alt="descricao">
        <MudarImagem @mudar-imagem="trocarImagem" />
    </div>
</template>
<script>
import MudarImagem from './MudarImagem.vue'
export default{
    name: 'Picture',
    data(){
        return{
            avatar: "/img/avatar.png",
            descricao: 'Vag profile picture',
            trocado: false
        }
    },
    components: {
        MudarImagem
    },
    methods: {
        trocarImagem(){
            this.trocado = !this.trocado
            if(!this.trocado){
                this.avatar = "/img/avatar2.png"
            }else{
                this.avatar = this.avatar = "/img/avatar.png"
            }
        }
    }
}
</script>