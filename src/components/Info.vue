<template>
  <div>
    <p v-if="esta_trabalhando"> Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades!</p>
  <p>Utilizo as seguintes tencologias:</p>
  <ul>
    <li>PHP</li>
  <li>Csharp</li>
  <li>Javascript</li>
  <li>Typescript</li>
  </ul>
  <div>
    <button @click="esta_trabalhando =!esta_trabalhando">Trabalhando?</button>
    <button @click="mostrar_email =!mostrar_email">{{ Mostrar_Email }}</button>
  </div>
  <p v-show="mostrar_email" >Mande uma mensagem para: {{ email }}</p>
  <p>Para acessar meu portfólio <a v-bind:href="Github" target="_blank"> basta clicar aqui</a></p>
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
data(){
  return{
esta_trabalhando: false,
mostrar_email: true,
email: 'email@gmial.com',
Github: 'https://github.com/guiorozimbo',
Mostrar_Email:"Mostrar Email"
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