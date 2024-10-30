<template>
  <div>
    <Header />
    <FirstComponent/>
    <p class="parag-pai">O dado de app é: {{ message }}</p>
    <LifeCycle/>
    <Pessoa/>

  </div>

</template>

<script>
import Header from './components/Header.vue'
import FirstComponent from './components/FirstComponent.vue'
import Info from './components/Info.vue';
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue';


export default {
  name: 'App',
  components: { 
    FirstComponent,
    LifeCycle,
    Pessoa,
    Header
  },
  data(){
    return {
      message: 'Hello Vue.js!'
    }
  }
}
</script>
<style>
body{
  background-color: #333;
  color: #fff;
  font-family: Arial;
  font-size: 16px;
  padding: 10px;
  margin: 0;
}
a{
  color: #675367;
  text-decoration: none;
}
.teste{
  background-color: black;
}

</style>