<script lang="ts">

import { createEventDispatcher } from 'svelte';
const dispatch = createEventDispatcher()

    let newdata: string = ""

    const submit = () => {
        dispatch("submit", {
        value: newdata
    })
        newdata = ""
    }
</script>

<div class="mt-4 w-1/3 p-2 bg-slate-300 rounded-lg flex justify-between">
    <input id="hello-world" type="text" class="w-full outline-none focus:bg-gray-50 p-2" bind:value={newdata}/>
    <button class="transition-all w-max p-2 bg-green-400 hover:bg-green-500" on:click={submit}>Submit</button>
</div>