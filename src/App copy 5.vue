<template>
  <div id="app">
   <!-- <h1 v-if="state === 'loading'">Loading</h1>
   <h1 v-else-if="state === 'error'">Error</h1>
   <h1 v-else-if="messages.length === 0">Sem dados disponíveis</h1>
   <h1 v-else>{{ messages }}</h1> -->
   <a :href="url">Site</a>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      state: 'comleted',
      messages: ['teste'],
      url: 'https://www.google.com.br'
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
