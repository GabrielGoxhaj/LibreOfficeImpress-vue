<template>
    <div id="dropdownDiapositiva" class="dropdownDiapositiva" :style="style">
        <a>Nuova diapositiva</a>
        <a>Duplica diapositiva</a>
        <a>Inserisci diapositiva da Diapositiva...</a>
        <a>Layout</a>
        <a>Elimina diapositiva</a>
        <hr />
        <a>Salva immagine di sfondo</a>
        <a>Imposta immagine di sfondo...</a>
        <a>Proprietà della diapositiva...</a>
        <hr />
        <a>Cambia schema diapositiva...</a>
        <a>Ruota schema</a>
        <a>Elimina schema</a>
        <hr />
        <a>Sfondo dello schema</a>
        <a>Oggetti dello schema</a>
        <a>Elementi dello schema...</a>
        <hr />
        <a>Mostra diapositiva</a>
        <a>Nascondi diapositiva</a>
        <a>Rinomina la diapositiva...</a>
        <hr />
        <a>Vai all'ultima diapositiva modificata</a>
        <a>Sposta</a>
        <a>Naviga</a>
        <hr />
        <a>Diapositiva sommario</a>
        <a>Pagina da struttura</a>
        <a>Cambio diapositiva</a>
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
.dropdownDiapositiva {
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

.dropdownDiapositiva a {
    color: black;
    text-decoration: none;
    font-family: 'Segoe UI', Tahoma, sans-serif;
    font-size: 9pt;
    display: block;
    margin-top: 1px;
    margin-left: 2px;
    padding-left: 7px;
    padding-top: 3px;
    padding-bottom: 3px;
    padding-right: 10px;
    transition: 0.1s;
    cursor: default;
}

.dropdownDiapositiva a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownDiapositiva a div img {
    margin-right: 14px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownDiapositiva a:hover {
    background-color: #95cdfb;
}

hr {
    margin: 0;
    color: #d7d7d7;
}
</style>