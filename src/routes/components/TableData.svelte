<script lang="ts">
    export let datas: string[]

    const handleDelete = (i: number) => {
        datas.splice(i, 1)
        datas = datas
    }
</script>

<div class="mt-4 p-2 w-1/3 bg-slate-300 rounded-lg">
    <h1 class="uppercase p-2 font-bold text-lg text-slate-600">{#if datas.length === 0} There is no task to do {:else} Todo list{/if}</h1>
    {#each datas as data, i (i)}
    <div class="mt-1 p-1 rounded flex items-center justify-between w-full bg-gray-50">
        <span>{data}</span>
        <button type="button" class="bg-red-300 text-xs rounded-xl p-2 hover:bg-red-400" on:click={() => handleDelete(i)}>Delete</button>
    </div>
    {/each}
</div>