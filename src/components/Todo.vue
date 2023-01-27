<script>
import TodoHeader from './TodoHeader.vue';
import NewTodo from './NewTodo.vue';
import TodoList from './TodoList.vue';

export default {
    components: {
        TodoHeader,
        NewTodo,
        TodoList
    },
    data() {
        return {
            todos: []
        }
    },
    methods: {
        addItem(item) {
            const newItem = {
                content: item,
                state: false
            };
            this.todos.push(newItem);
        },
        removeItem(index) {
            if (confirm("Are you sure to delete this todo item?"))
                this.todos.splice(index, 1);
        },
        changeItem(index){
            this.todos[index].state = !this.todos[index].state;
        }
    }
}

</script>

<template>
    <div class="md:container md:mx-auto">
        <TodoHeader />
        <div class="flex flex-col items-center">
            <NewTodo :addItem="addItem" />
            <TodoList :todos="todos" :removeItem="removeItem" :changeItem="changeItem" />
        </div>
    </div>
</template>

<style>

</style>