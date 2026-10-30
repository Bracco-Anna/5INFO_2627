<script>
    export let titolo;
    export let valori;

    import Item from "./item.svelte";

    console.log("VALORI:", valori)
</script>

<div class="contenitore">
    <div class="dropdown">
        {titolo}
    </div>
    <div class="items">
        {#each valori as valore}
            <Item titolo={valore} />
        {/each}
    </div>
</div>

<style>
.dropdown{
    background-color: red;
    width: 300px;
    height: 40px;
    border: 20px;
    padding-bottom: 20px;
    padding-left: 10px;
    padding-top: 20px;
    margin: 20px;
}

</style>


