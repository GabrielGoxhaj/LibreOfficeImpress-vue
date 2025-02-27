<template>
    <div id="dropdownStrumenti" class="dropdownStrumenti" :style="style">
        <a>Controllo ortografico...</a>
        <a>Controllo ortografico automatico</a>
        <a>Sinonimi...</a>
        <a>Lingua</a>
        <hr />
        <a>Opzioni di correzione automatica...</a>
        <hr />
        <a>Oscura</a>
        <a>Oscura in automatico</a>
        <hr />
        <a>Minimizza presentazione...</a>
        <a>Mappa immagine</a>
        <a>Sostituzione colore</a>
        <a>Lettore multimediale</a>
        <hr />
        <a>Formulari</a>
        <a>Macro</a>
        <a>Strumenti per lo sviluppo</a>
        <hr />
        <a>Impostazioni filtro XML...</a>
        <a>Estensioni...</a>
        <a>Personalizza...</a>
        <a>Opzioni...</a>
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
.dropdownStrumenti {
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

.dropdownStrumenti a {
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

.dropdownStrumenti a:hover {
    background-color: #91C9F7;
}
</style>