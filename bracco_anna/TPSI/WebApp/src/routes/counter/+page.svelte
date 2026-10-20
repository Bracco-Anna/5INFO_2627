<script>
    import Counter from "#lib/counter.svelte";
    import DoubleCounter from "#lib/components/who_am_i/DoubleCounter.svelte";

    let valore_singolo = 0
    let valore_doppio = 0
</script>
<h1>Pagina counter</h1>

{#if valore_singolo < 5}
    <h2 class="rosso">il valore del contatore vale: {valore_singolo}</h2>
{:else}
    <h2 class="verde">il valore del contatore vale: {valore_singolo}</h2>
{/if}

{#if valore_doppio < 5}
    <h2 class="rosso">il valore del contatore vale: {valore_doppio}</h2>
{:else}
    <h2 class="verde">il valore del contatore vale: {valore_doppio}</h2>
{/if}


<Counter bind:counter={valore_singolo}/>
<DoubleCounter bind:counter={valore_doppio}/>

<style>
    .rosso {color: #e797ab;}
    .verde {color: #e435d5;}
</style>