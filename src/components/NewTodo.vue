<script>

export default {
  props: {
    addItem: { type: Function },
  },
  methods: {
    addItem(){
        if(this.current !== "")
            this.addItem(this.current);
        this.current = '';
    }
  },
  data() {
    return { current: '' };
  }
}

</script>

<template>
    <div>
        <input type="text" v-model="current"
            class="bg-transparent border border-solid border-white rounded-md px-5 py-2 text-white text-lg mr-10"
            placeholder="New task" />
        <button
            class="bg-transparent border border-solid rounded-md border-white px-5 py-2 text-lg text-white transition-all duration-100 hover:px-10" @click="() => addItem()">Add</button>
    </div>
</template>

<style>

</style>