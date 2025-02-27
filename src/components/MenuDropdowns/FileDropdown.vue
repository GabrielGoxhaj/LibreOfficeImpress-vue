<template>
    <div id="dropdownFile" class="dropdownFile" :style="style">
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-nuovo.png">Nuovo</div><g>&#x1F782;</g></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-apri.png"> Apri...</div></a>
        <a>Apri in remoto...</a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-documenti-recenti.png">Documenti recenti</div><g>&#x1F782;</g></a>
        <a>Chiudi</a>
        <hr />
        <a style="display: flex; justify-content: space-between;">Procedure guidate<g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-modelli.png">Modelli</div><g>&#x1F782;</g></a>
        <hr />
        <a>Ricarica</a>
        <a>Versioni</a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-salva.png">Salva</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-salva-con-nome.png">Salva con nome...</div></a>
        <a>Salva in remoto...</a>
        <a>Salva una copia...</a>
        <a>Salva tutto</a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-esporta.png">Esporta</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-esporta.png">Esporta come</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;">Invia<g>&#x1F782;</g></a>
        <a>Anteprima nel browser web</a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-stampa.png">Stampa</div></a>
        <a>Impostazioni stampante...</a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-proprietà.png">Proprietà</div></a>
        <a style="display: flex; justify-content: space-between;">Firme digitali<g>&#x1F782;</g></a>
        <hr />     
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/file/file-esci.png">Esci da Libre Office</div></a>
    </div>
</template>

<script>

export default {
    props: {
        style: {
            type: Object,
            default: () =>({})
        }
    }
}
</script>

<style scoped>
.dropdownFile {
    position: absolute;
    background-color: #F2F2F2;
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
    padding-left: 5px;
    padding-top: 1px;
    padding-bottom: 4px;
    padding-right: 10px;
    transition: 0.1s;
    cursor: default;
}

.dropdownFile a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownFile a div img {
    margin-right: 5px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownFile a:hover {
    background-color: #91C9F7;
}

hr {
    margin: 0;
    color: #d7d7d7;
}
</style>