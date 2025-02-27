<template>
    <div id="dropdownFormato" class="dropdownFormato" :style="style">
        <a>Testo</a>
        <a>Spaziatura</a>
        <a>Allinea testo</a>
        <a>Elenchi</a>
        <hr />
        <a>Cancella formattazione diretta</a>
        <a>Stili</a>
        <hr />
        <a>Carattere...</a>
        <a>Paragrafo...</a>
        <a>Elenchi puntati e numerati...</a>
        <a>Tema...</a>
        <hr />
        <a>Tabella</a>
        <a>Immagine</a>
        <a>Casella di testo e forma</a>
        <a>Ombra</a>
        <hr />
        <a>Interazione...</a>
        <a>Nome...</a>
        <a>Alt Text...</a>
        <hr />
        <a>Distribuisci la selezione</a>
        <a>Ruota</a>
        <a>Ribalta</a>
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
.dropdownFormato {
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

.dropdownFormato a {
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

.dropdownFormato a:hover {
    background-color: #91C9F7;
}
</style>