<script setup>
import TodoHeader from './TodoHeader.vue';
import NewTodo from './NewTodo.vue';
import TodoList from './TodoList.vue';
import { ref, onMounted } from 'vue'

const todos = ref([]);

</script>

<template>
    <div class="md:container md:mx-auto">
        <TodoHeader />
        <div class="flex flex-col items-center">
            <NewTodo />
            <TodoList todos />
        </div>
    </div>
</template>

<style>

</style>