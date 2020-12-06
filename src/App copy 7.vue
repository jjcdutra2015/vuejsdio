<template>
  <div id="app">
    <!-- <button @click="count1++">Click1 {{ count1 }}</button>
    <button @click.ctrl="increment">Click2 {{ count2 }}</button>
    <button @click="increment2(2, $event)">Click3 {{ count3 }}</button>
    <input type="text" @keyup.alt.67="increment" /> -->
    <ListItem />
    {{ count2 }}
  </div>
</template>

<script>
import ListItem from './ListItem'
export default {
  name: "App",
  components: { ListItem },
  data() {
    return {
      text: '',
      count1: 0,
      count2: 0,
      count3: 0
    };
  },
  created() {
    this.$root.$on('increment', this.increment)
  },
  methods: {
    increment(valor, evento) {
      console.log(evento)
      this.count2 += valor
    },
    increment2(quantidade, event) {
      console.log(event)
      this.count3 += quantidade
    }
  }
};
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
