<template>
    <div
        class="grid justify-center justify-items-center font-serif rounded w-80 p-5 m-10 bg-gradient-to-r from-red-200 to-blue-400">
        <h1 class="font-bold text-2xl">Sign in</h1>
        <!-- <p>Add to bucket list</p> -->
        <br />
        <form class="flex">
            <div class="border border-solid border-slate-500 bg-slate-100 rounded font-serif p-4">
                <div>
                    <label>UserName :</label>&nbsp;
                    <input type="text" class="border border-solid border-slate-500 " />
                </div>
                <br />
                <div>
                    <label>Password :</label>&nbsp;
                    <input type="password" class="border border-solid border-slate-500 " />
                </div>
                <br />
                <div>
                    <button
                        class="float-right border border-2 border-solid bg-blue-600 rounded-lg text-white p-1 font-serif border-black hover:bg-blue-800">
                        <NuxtLink to="./form">Login</NuxtLink>
                    </button>
                </div>
            </div>
        </form>
    </div>
</template>
<script>
export default {
    name: 'AddTodo component'
}
</script>