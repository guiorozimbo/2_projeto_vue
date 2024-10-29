<template>
  <div>
    <h2>Meu formulário:</h2>
    <form action="" @submit="enviarForm($event)">
  <div>
   <input type="text" v-model="name">
  </div>
  
  <div>
    <input type="text" v-model="email">
  </div>
  
 <div>
   <Submit/>
 </div>
  </form>
  <p>aa</p>
  <p>aa</p>
  <p>aa</p>
  </div>

</template>
<script>
import InputText from './form/InputText.vue';
import Submit from './form/Submit.vue';
export default {
  name:'Form',
  components: {
    InputText,
    Submit
  }, 
  data(){
    return {
      name: '',
      email: ''
    }
  },

  methods: {
    enviarForm(e){ 
      const name = this.name;
      const email = this.email;
      e.preventDefault();
      console.log('enviar form')
      console.log("O nome é:"+name)
      console.log("O email é:"+email)
    }
  }
}
</script>

<style>
p{
  padding: 50px;
}

</style>