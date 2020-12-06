<template>
    <!-- <li @click="$emit('increment', 5, $event)">Click me</li> -->
    <li @click="emit">Click me</li>
</template>

<script>
export default {
    name: 'ListItem',
    methods: {
        emit(event) {
            this.$root.$emit('increment', 5, event)
        }
    }
}
</script>