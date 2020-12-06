<template>
  <div id="app">
    <Title />
  </div>
</template>

<script>
import Title from './Title'

export default {
  name: 'App',
  components: {Title},
  data() {
    return {
      
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
