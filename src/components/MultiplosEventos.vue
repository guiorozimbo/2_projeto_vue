<template>
  <div>
<button @click="primeiro(txt1,$event), segundo(txt2,$event),terceiro(txt3,$event)">Ativar mútiplos Eventos</button>
<p>{{ multiplos_eventos }}</p>
  </div>
</template>
<script>
export default {
name: 'MultiEventos',
  data: () => {
    return {
      multiplos_eventos: '',
      txt1: 'Primeiro Evento',
      txt2: 'Segundo Evento'
    }
  },
  methods: {
    primeiro(txt,e) {
      this.multiplos_eventos = txt
      
    },
    segundo(txt,e) {
   setTimeout(() => this.multiplos_eventos = txt, 2000)
    
  },
  terceiro(txt,e) {
    setTimeout(() => this.multiplos_eventos = "", 4000)
  }
}
  }
  
</script>

<style scoped>
div {
  margin: 100px;
}
</style>