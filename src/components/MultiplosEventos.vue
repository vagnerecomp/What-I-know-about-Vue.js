<template>
    <!-- Conteúdos abordados: Trabalhando com multiplos eventos -->
    <div>
        <button @click="first($event), second($event), third($event), clear($event)">Ativar multtiplos eventos</button>
        <p>{{multiplos_eventos}}</p>
    </div>
</template>

<script>
export default {
    name: 'MultiplosEventos',
    data(){
        return{
            multiplos_eventos: "",
            txt1: 'Primeiro evento',
            txt2: 'Segundo evento'
        }
    },
    methods:{
        first(e){
            this.multiplos_eventos = this.txt1
        },
        second(e){
            setTimeout(()=>{
                this.multiplos_eventos = this.txt2
            }, 1000)
        },
        third(e){
            setTimeout(()=>{
                this.multiplos_eventos = this.txt1 + " " + this.txt2
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