<template>
    <div class=" flex flex-col items-center bg-gradient-to-r from-red-200 to-blue-400 w-80 ml-10">
        <div class="m-2 p-2 bg-slate-200 w-64 ">
            <p>
                <input type="checkbox" v-on:click="checked" />
                {{ items.Title }}
                <button @click="$emit('delete-todo', items.id)" class="del font-serif font-semibold float-right bg-red-600 rounded-md text-white p-1 m-1">Delete</button>
                <button @click="update" class="font-serif font-semibold float-right bg-blue-600 rounded-md text-white p-1 m-1">Edit</button>
            </p>
        </div>
        <div v-if="this.flag">
            <form @submit="updatetodo">
                <div>
                    <input type="text" v-model="updateTitle" placeholder="Title" required />
                </div>
                <div>
                    <button class="float-left font-serif font-semibold bg-blue-700 rounded-md text-white p-1 m-1">
                        Update
                    </button>
                </div>
            </form>
        </div>
    </div>
</template>
<script>
export default {
    name: 'todoitem component',
    props:['items','dataarray'],
    methods: {
        update() {
            this.flag = !this.flag;
        },
        updatetodo(e) {
            e.preventDefault()
            this.dataarray.filter((items) => {
                if (items.id == this.items.id) {
                    //update the title
                    items.Title = this.updateTitle
                }
            })
            //reset the flag
            this.flag = false
        }

    },
    data() {
        return {
            flag: false,
            updateTitle: ""
        }
    }
}
</script>