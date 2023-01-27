<script>
export default {
    props: {
        todo: {
            type: Object
        },
        index: {
            type: Number
        },
        removeItem: {
            type: Function
        }
    }
}
</script>

<template>
    <div class="mt-3 text-white text-2xl flex items-center justify-around">
        {{ this.todo.content }}
        <button class="ml-5 border border-solid border-white rounded-md px-5 py-2 bg-transparent text-lg"
            @click="() => this.removeItem(this.index)">remove</button>
    </div>
</template>

<style>

</style>