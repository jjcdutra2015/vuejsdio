<template>
  <div id="app">
    <button @click="fullNameComputed = 'Carvalho Dutra'">Clicar</button>
    {{ fullNameComputed }}
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      firstName: 'Julio',
      lastName: 'Dutra'
    }
  },
  computed: {
    fullNameComputed: {
      get() {
        return `${this.firstName} ${this.lastName}`
      },
      set(value) {
        const [first, last] = value.split(' ')
        this.firstName = first
        this.lastName = last
      }
    }
  },
  methods: {
    fullName() {
      return `${this.firstName} ${this.lastName}`
    }
  },
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
