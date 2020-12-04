<template>
    <button @click="click">Clicar ButtonVue {{ count }} times </button>
</template>

<script>
export default {
    data() {
        return {
            count: 0
        }
    },
    methods: {
        click() {
            this.count++
        }
    }
}
</script>