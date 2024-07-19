<template>
  <div>
    <h1 :class = "{'title': true, 'title-home':isHome}">
      Curso Vue 3
    </h1>



    <div>
      <button @click.once="onClick">
        Enviar, com teste
      </button>
      <br>

      <div @mouseover="onMouseOver"
           @mouseout="onMouseOut">
        Mouse Over
      </div>
      <br>
      <form 
        action="https://google.com"
        @submit.prevent="onSubmit"
      >
        <input
          type="text"
          @keyup.enter="onKeyup"
        >
        <button type="submit">
          Enviar
        </button>
      </form>
    </div>

    <div>
      One-way data binding <br>
      Two-way data binding <br>
      v-model -> formulários
    </div>
    
    <br>

    <div>
      <label> Inserção de dados </label><br>
      <input
      v-model="name"
      type="text"
      ><br>
      {{ name }}
    </div>
    
    <br>

    <div>
      <label>Sports</label><br>
      <select v-model="sports">
        <option value="">Escolha</option>
        <option value="Data Science">Data Science</option>
        <option value="Desenvolvimento">Desenvolvimento</option>
        <option value="Infra">Infra</option>
      </select><br>
      {{ sports }}
    </div>
    
    <br>

    <div>
      <label>Newsletter</label><br>
      <input
        v-model="newsletter"
        type="radio"
        value="Sim"
      > Sim
      <input
        v-model="newsletter"
        type="radio"
        value="Não"
      > Não
      <br>
      {{newsletter}}
    </div>

    <div>
      <label>Contrato</label><br>
      <input
        v-model="contract"
        type="checkbox"
      > Concordo e aceito os termos...
      <br>
      {{contract}}
    </div>
    
    <br>

    <div>
      <label>Cores que você mais gosta</label><br>
      <input
        v-model="colors"
        type="checkbox"
        value="Azul"
      > Azul
      <input
        v-model="colors"
        type="checkbox"
        value="Amarelo"
      > Amarelo
      <br>
      {{colors}}
    </div>
    <br>
    <div>
      <label>Contrato</label><br>
      <input
        v-model="contract"
        type="checkbox"
      > Concordo e aceito os termos...
      <br>
      {{contract}}
    </div>


    <p :class="[pClass]">
      Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado. Se popularizou na década de 60, quando a Letraset lançou decalques contendo passagens de Lorem Ipsum, e mais recentemente quando passou a ser integrado a softwares de editoração eletrônica como Aldus PageMaker
    </p>

    <p :style="styleClass">
    Ao contrário do que se acredita, Lorem Ipsum não é simplesmente um texto randômico. Com mais de 2000 anos, suas raízes podem ser encontradas em uma obra de literatura latina clássica datada de 45 AC. Richard McClintock, um professor de latim do Hampden-Sydney College na Virginia, pesquisou uma das mais obscuras palavras em latim, consectetur, oriunda de uma passagem de Lorem Ipsum, e, procurando por entre citações da palavra na literatura clássica, descobriu a sua indubitável origem. Lorem Ipsum vem das seções 1.10.32 e 1.10.33 do "de Finibus Bonorum et Malorum" (Os Extremos do Bem e do Mal), de Cícero, escrito em 45 AC. Este livro é um tratado de teoria da ética muito popular na época da Renascença. A primeira linha de Lorem Ipsum, "Lorem Ipsum dolor sit amet..." vem de uma linha na seção 1.10.32.
    </p>


    <h1>{{ msg }}</h1>
    <p>
      This page was made to test Vue js.
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Social Network</h3>
    <ul>
      <li><a href="https://econocargo.com.br/" target="_blank" rel="noopener">Site Econocargo</a></li>
      <li><a href="https://github.com/CarlosHenriqueMatos" target="_blank" rel="noopener">Repositorio do projeto</a></li>
    </ul>
    <h3>More about Vue js</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return{classVar:'title',
          name: 'Informe o seu nome',
          sports: "",
          newsletter: '',
          contract: false,
          pClass: ['text', 'text-home'],
          styleClass:{'color':'white', 'backgroundColor':'black', 'font-size':'20px'},
          isHome:true,
          colors:[]
    }
  },  
  methods:{
    onClick($evt){
      console.log('click',$evt);
    },
    onMouseOver($evt){
      console.log('mouse over', $evt);
    },
    onMouseOut($evt){
      console.log('mouse out', $evt);
    },
    onSubmit($evt){
      console.log('submit', $evt);
    },
    onKeyup($evt){
      console.log('onKeyup', $evt);

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.title{
        font-size: 20px;
        color: blue;
    }
    .title-home{
      font-size: 40px;
      color: green;
    }
    .text {
      color:blue;
    }
</style>
