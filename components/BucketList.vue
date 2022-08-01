<template>
    <div class="grid justify-items-center font-serif rounded w-80 p-5 m-10 bg-gradient-to-r from-red-200 to-blue-400">
        <h1 class="text-center font-bold">ToDos App </h1>
        <br />
        <form @submit="addTododata" class="grid justify-items-left bg-slate-200 p-7 w-64">
            <div>
                <input type="text" v-model="Title" placeholder="Title" required />
            </div>
            <br />
            <div>
                <button class=" bg-blue-700 border-1 border-black text-white p-1 rounded-md font-serif font-semibold ">
                    Add</button>
            </div>
        </form>
    </div>
</template>
<script>
    export default{
        name:'Bucketlist component',
        data(){
            return{
                Title:''
            }
        },
        methods:{
            addTododata(e){
                e.preventDefault()
                const newTodo = {
                    id:Date.now(),
                    Title: this.Title,
                    completed:false
                }

                this.$emit("add-todo", newTodo)
                this.Title = '';
            }
        }
    }
</script>