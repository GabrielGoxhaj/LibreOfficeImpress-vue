<template>
    <div id="dropdownModifica" class="dropdownModifica" :style="style">
        <a>Annulla</a>
        <a>Ripristina</a>
        <hr />
        <a>Taglia</a>
        <a>Copia</a>
        <a>Incolla</a>
        <a>Incolla speciale</a>
        <hr />
        <a>Duplica</a>
        <a>Seleziona tutto</a>
        <hr />
        <a>Trova...</a>
        <a>Trova e sostituisci...</a>
        <hr />
        <a>Toggle Point Edit Mode</a>
        <a>Punti di incollaggio</a>
        <hr />
        <a>Collegamento ipertestuale</a>
        <a>Campi...</a>
        <a>Collegamenti esterni...</a>
        <a>Oggetto OLE</a>
        <hr />
        <a>Modo Modifica</a>
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
.dropdownModifica {
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

.dropdownModifica a {
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

.dropdownModifica a:hover {
    background-color: #91C9F7;
}
</style>