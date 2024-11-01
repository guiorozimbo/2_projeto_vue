<template>
  <div>
    <button @click="$emit('mudarImagem')">
Trocar Imagem de perfil
    </button>
  </div>
</template>
<script>
export default {
  name: 'BotaoImagem',
  emits: ['mudarImagem']
}
</script>