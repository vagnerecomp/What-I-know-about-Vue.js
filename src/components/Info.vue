<template>
    <!-- Conceitos abordados: Diretivas v-if, v-else e v-show
        componentização, argumentos dinâmicos, métodos, renderização de listas com v-for, props -->
    <div>
        <!-- Uso das diretivas v-if e v-else -->
 
        <p v-if="esta_trabalhando">Eu estou trabalhando atualmente</p>
        <p v-else>Estou em busca de oportunidades</p>
        
        <p>Utilizo as seguntes techs para back-end:</p>
        <ul>
            <li v-for="(tech, index) in backend_technologies" v-bind:key="index">{{tech}}</li>
        </ul>

        <p>Utilizo as seguintes techs para front-end:</p>
        <ul>
            <li v-for="tech in frontend_technologies" :key="tech.id">
                {{tech.language}}
            </li>
        </ul>


        <!-- Botão mostra ou ocultar email usando evento e método -->
        <div>
            <button @click="showEmail">{{textoBotao}}</button>
        </div>
        <!-- Uso da diretiva v-show -->
        <p v-show="mostrar_email">Mande um email para: {{compEmail}}</p> <!-- compEmail é uma props que vem do componente Pessoa.vue-->
        <p>Você pode ver o meu portifólio <a :href="meu_link" target="_blank"> clicando aqui</a></p>
        <Picture/>
    </div>
</template>
<script>
import Picture from './Picture.vue';
export default {
    name: 'Info',
    components:{
        Picture
    },
    props: {
        compEmail: String
    },
    data(){
        return{
            
            esta_trabalhando: false,
                /* Se o valor dessa propriedade for 'true' a frase "Estou trabalhando atualmente"
                vai ser exibida, se for false, a frase "Estou em busca de oportunidades" vai ser
                exibida em seu lugar.*/
            
            email: 'vagnerecomp@gmail.com',
            mostrar_email: false,
                /*Se o valor dessa prop for verdadeiro o email sera exibido,
                senão, não será exibido porque do atributo v-show*/
            meu_link: 'https://www.google.com',
            textoBotao: "Mostrar e-mail",
            
            // dados para v-for:
            backend_technologies: ['Java', 'Python', 'Node.js'],
            frontend_technologies: [
                {id:0, language: 'HTML'},
                {id:1, language: 'CSS'},
                {id:2, language: 'Vue.js'}
            ]
        }
    },
    methods: {
        // O método showEmail é chamado pelo evento @click e se encarrega de
        // alterar os dados passados como valor para o v-show sempre que houver click
        // Além disso, ele verifica o  valor do dado mostrar_email para alterar o texto
        // do botão de acordo com esse valor.
        showEmail(){
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email){
                this.textoBotao = "Mostrar e-mail"
            }else{
                this.textoBotao = "Esconder e-mail"
            }
        }
    }
}
</script>