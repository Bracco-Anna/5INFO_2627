<script>
import Dropdown from "#lib/components/dropdown.svelte";
</script>

<h1>DROPDOWN TESTER </h1>

<Dropdown 
    titolo='regione' 
    valori={['Piemonte', 'Lombardia', 'Veneto', 'Lazio']} 
/>


<Dropdown titolo='città'/>

<Dropdown titolo='Nazione' />