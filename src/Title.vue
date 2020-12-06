<template>
  <div>
    <h1>{{ titulo }}</h1>
    <h2>{{ subtitulo }}</h2>
    <h3>{{ tipo }}</h3>
  </div>
</template>

<script>
export default {
  name: "Title",
  inheritAttrs: false,
  props: {
    titulo: String,
    subtitulo: String,
    tipo: Number
  },
  data() {
    return {};
  },
};
</script>