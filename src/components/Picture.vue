<template>
  <div>
    <img :src="image" :alt="descricao" >
    <reutilizacao/>
  </div>
</template>
<script>
import Reutilizacao from './Reutilizacao.vue'
export default {
  components: { Reutilizacao },
  name: 'Image',
  data () {
    return {
      image: '/img/b2bb0c6d-8d16-4c67-9bff-35a95dc72c03-a39defda26f86f397417292651321436-640-0.webp',
      descricao: "Tupac shakur"
    }
  }
}
</script>