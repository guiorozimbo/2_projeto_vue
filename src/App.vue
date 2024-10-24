<template>
  <div>
    <FirstComponent/>
    <p>O dado de app é: {{ message }}</p>
    <LifeCycle/>
    <Pessoa/>
    
  </div>
  
</template>

<script>
import FirstComponent from './components/FirstComponent.vue'
import Info from './components/Info.vue';
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue';


export default {
  name: 'App',
  components: { 
    FirstComponent,
    LifeCycle,
    Pessoa
  },
  data(){
    return {
      message: 'Hello Vue.js!'
    }
  }
}
</script>