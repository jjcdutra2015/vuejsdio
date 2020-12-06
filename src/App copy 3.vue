<template>
  <div id="app">
    <input type="text" v-model="text">
    <span>{{text}}</span>
    <span>{{apiResponse}}</span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      apiResponse: 'Start',
      text: ''
    }
  },
  methods: {
    simulateApi(response) {
      return new Promise((res) => {
        setTimeout(() => {
          this.apiResponse = response
        }, 1000)
      })
    },
    async fetchApi(value) {
      await this.simulateApi(value)
    },
  },
  watch: {
    text(val, old) {
      console.log(val, old)
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
