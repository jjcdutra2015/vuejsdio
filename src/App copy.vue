<template>
  <div id="app">
    <ButtonVue></ButtonVue>
    <ButtonString></ButtonString>
    <ButtonTemplateString></ButtonTemplateString>
    <ButtonXTemplate></ButtonXTemplate>
    <ButtonInline inline-template>
      <button @click="click">Clicar ButtonInline {{ count }} times </button>
    </ButtonInline>
    <ButtonRender></ButtonRender>
    <ButtonJSX></ButtonJSX>
  </div>
</template>

<script>
import ButtonVue from './ButtonVue'

export default {
  name: 'App',
  components: {
    ButtonVue
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
