<template>
    <div class=" flex flex-col items-center bg-gradient-to-r from-red-200 to-blue-400 w-80 ml-10">
        <div class="m-2 p-2 bg-slate-200 w-64 ">
            <p>
                <input type="checkbox" />
                {{ items.Title }}
                <button class="del font-serif font-semibold float-right bg-red-600 rounded-md text-white p-1 m-1">Delete</button>
                <button class="font-serif font-semibold float-right bg-blue-600 rounded-md text-white p-1 m-1">Edit</button>
            </p>
        </div>
    </div>
</template>
<script>
export default {
    name: 'todoitem component',
    props:['items']
}
</script>