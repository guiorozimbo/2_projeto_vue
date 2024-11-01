<template>
  <div>
    <p>{{ email }}</p>
    <p v-if="esta_trabalhando"> Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades!</p>
  <p>Utilizo as seguintes tencologias para backend:</p>
  <ul >
    <li v-for="(techonology,index) in Backend_tecnologies" v-bind:key="index">{{techonology}}</li>
  
  </ul>
<p>Utilizo as seguintes tecnologias para front-end:</p>
<ul>
  <li v-for="(techonology) in front_tecnologies" :key="techonology.id">{{techonology.language}}</li>
</ul>
  <div>
    <button @click="esta_trabalhando =!esta_trabalhando">Trabalhando?</button>
    <button @click="mostrar_email =!mostrar_email">{{ Mostrar_Email }}</button>
  </div>
  <p v-show="mostrar_email" >Mande uma mensagem para: {{ email }}</p>
  <p class="teste">Para acessar meu portfólio <a v-bind:href="Github" target="_blank"> basta clicar aqui</a></p>
  <Picture/>
  </div>
</template>

<script >
import Picture from './Picture.vue'
export default{
name: 'Info',
components:{
  Picture
},
props:{
  nome: String,
  email:String,
  esta_trabalhando: Boolean,
},
data(){
  return{

mostrar_email: true,
Github: 'https://github.com/guiorozimbo',
Mostrar_Email:"Mostrar Email",
Backend_tecnologies:['PHP','C#','Javascript','Typescript'],
front_tecnologies:[{id: 1, language:'HTML'},{id:2,language:'CSS'},{id:3,language:'Sass'}],
  }
},
methods:{
  mostra_email(){
    if(this.mostrar_email == true){
      this.mostrar_email = false
    }else{
      this.mostrar_email = true
    }
  }
}
}
</script>

<style>
.parag-pai{
  color: rebeccapurple;
}
</style>