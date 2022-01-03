<template>
    <div>
        <button @click="ativar">Clique aqui</button>
        <span v-show="ativado">Ativado</span>
    </div>
</template>

<script>
export default {
    name: 'Reutilizacao',
    data(){
        return{
            ativado: false

        }
    },
    methods: {
        ativar(){
            this.ativado = !this.ativado
        }
    }
}

</script>