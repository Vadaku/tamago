<!-- Root Route e.g tamago.co.nz -->
<script>

    let exampleArr = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

</script>

<svelte:head>
    <title>TAMAGO</title>
</svelte:head>

<div id="example-container">
    {#each exampleArr as example}
        <div class="examples">

        </div>
    {/each}
</div>

<style>

    #example-container {
        height: 100%;
        width: 100%;
        display: flex;
        flex-wrap: wrap;
    }

    .examples {
        border: 1px solid black;
        height: 200px;
        width: 200px;
    }

</style>