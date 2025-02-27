<template>
    <div id="dropdownFile" class="dropdownFile" :style="style">
        <a>Nuovo</a>
        <a>Apri...</a>
        <a>Apri in remoto...</a>
        <a>Documenti recenti</a>
        <a>Chiudi</a>
        <hr />
        <a>Procedure guidate</a>
        <a>Modelli</a>
        <hr />
        <a>Ricarica</a>
        <a>Versioni</a>
        <hr />
        <a>Salva</a>
        <a>Salva con nome...</a>
        <a>Salva in remoto...</a>
        <a>Salva una copia...</a>
        <a>Salva tutto</a>
        <hr />
        <a>Esporta</a>
        <a>Esporta come</a>
        <a>Invia</a>
        <a>Anteprima nel browser web</a>
        <hr />
        <a>Stampa...</a>
        <a>Impostazioni stampante...</a>
        <hr />
        <a>Proprietà...</a>
        <a>Firme digitali</a>
        <hr />
        <a>Esci da LibreOffice</a>
    </div>
</template>

<script>
export default {
    props: {
        style: {
            type: Object,
            default: () => ({})
        }
    }
}
</script>

<style scoped>
.dropdownFile {
    position: absolute;
    background-color: #F2F2F2;
    padding: 2px;
    width: 255px;
    height: auto;
    overflow: auto;
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
    border: lightgray;
    border-width: 1px;
    border-style: solid;
    z-index: 10;
}

.dropdownFile a {
    color: black;
    text-decoration: none;
    font-family: 'Segoe UI', Tahoma, sans-serif;
    font-size: 9pt;
    display: block;
    padding-left: 30px;
    padding-top: 4px;
    padding-bottom: 4px;
    padding-right: 10px;
    transition: 0.1s;
}

.dropdownFile a:hover {
    background-color: #91C9F7;
}
</style>