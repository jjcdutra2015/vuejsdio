<template>
  <div id="app">
   <Title v-bind="titulos[0]" />
  </div>
</template>

<script>
import Title from './Title'

export default {
  name: 'App',
  components: { Title },
  data() {
    return {
     titulos:[
       { titulo: "Titulo1", subtitulo: "Sub", tipo: 5 }
     ]
    }
  }
}
</script>

<style>
#app {
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: center;
 height: 100vh;
}
</style>
