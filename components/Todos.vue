<template>
    <div>
        <div v-for="items in dataarray" :key="items.id">
            <!-- {{items.Title}} -->
            <TodoItem v-bind:dataarray="dataarray" v-bind:items="items" v-on:delete-todo="$emit('delete-todo', items.id)"></TodoItem>
        </div>
    </div>
</template>
<script>
import TodoItem from './TodoItem.vue'

    export default {
        name: 'Todos component',
        props:['dataarray'],
        components:{TodoItem}
    }
</script>