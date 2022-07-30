<template>
    <div>
        <div v-for="items in dataarray" :key="items.id">
            <!-- {{items.Title}} -->
            <TodoItem v-bind:items="items"></TodoItem>
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