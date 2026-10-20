
<script>
    let nome, cognome, eta, residenza;
    let confermato = false;
</script>
<h1>input page</h1>

Nome: <input bind:value={nome}><br>
Cognome: <input bind:value={cognome}><br>
Età: <input bind:value={eta}><br>
Residenza: <input bind:value={residenza}><br>
<br><br>
Confermato: <input type="checkbox" bind:checked={confermato}>
<br><br>
io sono {nome}{cognome} e ho {eta} anni, abito a {residenza}
<br><br>
<button disabled={!confermato}>Invia</button>