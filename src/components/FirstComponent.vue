<template>
 <div>
  <h1>Olá Vue!</h1>
  <p>Meu nomme é: {{ name }} e trabalho como {{ profissao }}</p>
 </div>
</template>

<script>

export default ({
name: 'Primeiro componente Vue',
data(){
  return {
    name: 'Guilherme',
    profissao: 'Desenvolvedor de software'
  }
}
})
</script>