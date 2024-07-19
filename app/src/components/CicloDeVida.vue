<template>
    <div>
        <TheHeader v-if="showHeader" />
        <h1>Hello World</h1>
        {{ name }} <br>
        <button @click="showHeader=true">
            Ativar e desativar header
        </button>
    </div>
</template>

<script>
import TheHeader from './TheHeader.vue';

export default{
    name: "App",
    components:{ TheHeader },
    data(){
        return{
            name: 'Jon Snow',
            snowHeader: true,

        }
    },

// Criação
    // Preparar o componente
    // Ajax, inicializar algumas variáveis
    // Não tem acesso ao template (DOM)
// Montagem
    // Inicializar um lib externa
    // Precisa de acesso ao template (DOM)
    // Tem acesso ao template (DOM)
// Atualização
    // Debug
    // Update
// Desmontagem
    // Remover tudo o que for necessario (lib->destroy())
    // para liberar memória
// HOOKS
    beforeCreate(){
        console.log('beforeCrate');
    },
    created(){
        console.log('created');
    },
    beforeMount(){
        console.log('beforeMount');
    },
    mounted(){
        console.log('mounted');
    },
    beforeUnmount(){
        console.log('beforeUnmount');
    },
    unmounted(){
        console.log('unmounted');
    },

watch:{
},

computed:{

},

methods: {
    activateHeader(){
        this.showHeader = false
    },
    deactivateHeader(){
        
    }
},

}

</script>

<style>
    .header{
        background: #000;
        color: #fff;
    }
</style>