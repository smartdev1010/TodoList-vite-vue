<script>
import TodoItem from './TodoItem.vue';
export default {
    props: {
        todos: { type: Array },
        removeItem: { type: Function }
    },
    components: {
        TodoItem
    }
}
</script>

<template>
    <div class="mt-10">
        <TodoItem v-if="this.todos.length > 0" v-for="(todo, index) in this.todos" :todo="todo" :index="index" :removeItem="this.removeItem" />
        <h1 v-else class="text-white text-2xl" >There are no todo lists.</h1>
    </div>
</template>

<style>

</style>