<script lang="ts">
    import "../style/app.css"
	import AddTodo from "./components/AddTodo.svelte";
    import Header from "./components/Header.svelte"
	import TableData from "./components/TableData.svelte";

    let datas: string[] = []

    function handler(e:any) {
        datas.push(e.detail.value)
        datas = datas
    }
</script>

<div class="min-h-screen bg-slate-400 flex flex-col items-center">
    <Header />
    <AddTodo on:submit={handler}/>
    <TableData datas={datas} />
</div>
