<template>
       <BucketList v-on:add-todo="addTododata"></BucketList>
       <Todos v-bind:dataarray="dataarray" v-on:delete-todo="deletetododata"></Todos>
</template>
<script>
import  BucketList  from '/components/BucketList.vue'
import Todos from '/components/Todos.vue'
    export default{
        name:'list page',
        components:{BucketList, Todos},
        data(){
        return{
            dataarray:[
                {
                    id:'1',
                    Title:"BList1",
                    completed:false
                },
                {
                    id:'2',
                    Title:"BList2",
                    completed:false
                }
            ]
        }  
    },
    methods:{
        addTododata(newTodo){
            this.dataarray = [...this.dataarray, newTodo]
        },
        deletetododata(id) {
      this.dataarray = this.dataarray.filter((items) => items.id !== id)
    }
    }
    
    }
</script>