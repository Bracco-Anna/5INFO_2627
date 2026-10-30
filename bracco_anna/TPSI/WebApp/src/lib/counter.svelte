<svelte:head>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" rel="stylesheet" />
<link href="https://fonts.googleapis.com/css?family=Bungee+Spice&display=swap" rel="stylesheet">
</svelte:head>
<script>
    import { createEventDispatcher } from "svelte";

    import { store_counter } from "./js/store";

    const dispatch = createEventDispatcher();
    export let counter = 0;

    function counter_incr(){
        counter += 1;
        $store_counter = counter;
        emit_event1('incr');
    }
    function counter_decr(){
        counter -= 1;
        $store_counter = counter
        emit_event2('decr');
    }
    function emit_event1(tipo){
        dispatch('contatore', {
            tipo: tipo,
            valore: counter
        })
    }
    function emit_event2(tipo2){
        dispatch('contatore', {
            tipo: tipo2,
            valore: counter
        })}
</script>
<div class="container">
    <div class="pulsante">
        <button on:click={counter_decr}>
         <span class="material-symbols-outlined icon">remove</span>
        </button>
    </div>
    <div class="number">
        {counter}
    </div>
    <div class="pulsante">
     <button on:click={counter_incr}>
        <span class="material-symbols-outlined icon">add</span>
     </button>
     </div>
    </div>
<style>
.container {
    border: 4px solid #f06df0;
    display: flex;
    justify-content: space-between;
    border-radius: 30px;
    width: 300px;
    padding: 10px;
    }
    .pulsante {
        display: flex;
        align-items: center;
    }
    button {
        border: none;
        background: none;
    }
    .icon {
font-size: 2.5rem;
color: #e605e6;
font-weight: bolder;
}
.icon:hover {
color: #f06df0;
cursor: pointer;
}
.icon:active {
text-shadow: 1px 1px 10px #f06df0;
}
.number {
font-size: 4rem;
font-family: 'Bungee Spice', cursive;
}
</style>

