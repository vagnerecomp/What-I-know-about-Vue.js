<template>
    <!-- Conteúdos abordados: Trabalhando com multiplos eventos, tornando os dados dos métodos dinâmicos -->
    <div>
        <button @click="first(txt1, $event), second(txt2, $event), third(txt3, $event), clear($event)">Ativar multtiplos eventos</button>
        <p>{{multiplos_eventos}}</p>
    </div>
</template>

<script>
export default {
    name: 'MultiplosEventos',
    data(){
        return{
            multiplos_eventos: "",
            txt1: 'Primeiro evento ativado',
            txt2: 'Segundo evento ativado',
            txt3: 'Terceiro ativado'
        }
    },
    methods:{
        first(txt, e){
            this.multiplos_eventos = txt
        },
        second(txt, e){
            setTimeout(()=>{
                this.multiplos_eventos = txt
            }, 1000)
        },
        third(txt, e){
            setTimeout(()=>{
                this.multiplos_eventos = txt
            }, 2000)
        },
        clear(e){
            setTimeout(()=>{
                this.multiplos_eventos = ""
            }, 3000)
        }
    }
}
</script>