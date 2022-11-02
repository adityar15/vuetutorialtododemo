<template>
    <form @submit.prevent="addTodo">
        <input type="text" v-model="todoText" />
        <button type="submit">Add</button>
    </form>
</template>

<script setup>
import {ref} from "vue"
const todoText = ref("")
const emit = defineEmits(['added'])

function addTodo()
{
    emit('added', todoText.value)
}

</script>

<style lang="scss" scoped>

</style>