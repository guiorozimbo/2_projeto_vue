<template>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Projetos</a></li>
    <li><a href="#">Contato</a></li>
    <li v-if="esta_logado"><a href="#">Meu perfil</a></li>
  </ul>
</template>

<script>
export default{
  name: 'Header',
  props: ['esta_logado']
}
</script>

<style scoped>
ul{
  display: flex;
  justify-content: space-around;
  align-items: center;
  list-style: none;
}
li{
  margin-right: 10px;
}
a{
  text-decoration: none;
  color: #fff;
  transition: .4s;
}
a:hover{
  color: turquoise;
  text-shadow: 0 0 3px #fff;
}
</style>