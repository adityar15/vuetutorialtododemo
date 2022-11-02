<template>
    <li>
        {{props.todo.text}}
    </li>
</template>

<script setup>

const props = defineProps({
    todo: Object
})

</script>

<style lang="scss" scoped>

</style>