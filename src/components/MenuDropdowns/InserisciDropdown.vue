<template>
    <div id="dropdownInserisci" class="dropdownInserisci" :style="style">
        <a>Immagine...</a>
        <a>Audio o video...</a>
        <a>Grafico...</a>
        <a>Tabella...</a>
        <a>Media</a>
        <a>Oggetto OLE</a>
        <a>Forma</a>
        <hr />
        <a>Linea guida di cattura...</a>
        <hr />
        <a>Casella di testo</a>
        <a>Commento</a>
        <a>Fontwork...</a>
        <hr />
        <a>Collegamento...</a>
        <a>Carattere speciale...</a>
        <a>Segno di formattazione</a>
        <hr />
        <a>Numero diapositiva</a>
        <a>Comando di campo</a>
        <a>Intestazione e piè di pagina...</a>
        <hr />
        <a>Controlli per formulari</a>
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
.dropdownInserisci {
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

.dropdownInserisci a {
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

.dropdownInserisci a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownInserisci a div img {
    margin-right: 5px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownInserisci a:hover {
    background-color: #91C9F7;
}

hr {
    margin: 0;
    color: #d7d7d7;
}
</style>