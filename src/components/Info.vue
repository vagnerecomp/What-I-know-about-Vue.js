<template>
    <!-- Conceitos abordados: Diretivas v-if, v-else e v-show
        componentização, argumentos dinâmicos -->
    <div>
        <!-- Uso das diretivas v-if e v-else -->
        <p v-if="esta_trabalhando">Eu estou trabalhando atualmente</p>
        <p v-else>Estou em busca de oportunidades</p>
        <p>Utilizo as seguntes techs:</p>
        <ul>
            <li>ReactJS</li>
            <li>VueJS</li>
            <li>NodeJS</li>
        </ul>
        <!-- Uso da diretiva v-show -->
        <p v-show="mostrar_email">Mande um email para: {{email}}</p>
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
    data(){
        return{
            
            esta_trabalhando: false,
                /* Se o valor dessa propriedade for 'true' a frase "Estou trabalhando atualmente"
                vai ser exibida, se for false, a frase "Estou em busca de oportunidades" vai ser
                exibida em seu lugar.*/
            
            email: 'vagnerecomp@gmail.com',
            mostrar_email: true,
                /*Se o valor dessa prop for verdadeiro o email sera exibido,
                senão, não será exibido porque do atributo v-show*/
            meu_link: 'https://www.google.com'
        }
    }
}
</script>