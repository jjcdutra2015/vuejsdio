<template>
  <div id="app">
    <!-- <input type="text" @input="text = $event.target.value" :value="text"> -->
    <!-- <input type="text" v-model.trim="text"> -->
    <Input v-model="text" />
    {{ text }}
  </div>
</template>

<script>
import Input from './Input'
export default {
  components: { Input },
  name: "App",
  data() {
    return {
      text: '',
    };
  },
  watch: {
    text(valor) {
      console.log(valor)
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
