<template>
    <div id="dropdownAiuto" class="dropdownAiuto" :style="style">
        <a>Guida di LibreOffice</a>
        <a>Cos'è questo?</a>
        <a>Guide utente</a>
        <a>Mostra suggerimento del giorno</a>
        <a>Cerca comandi</a>
        <hr />
        <a>Ottieni aiuto in linea</a>
        <a>Invia commenti...</a>
        <hr />
        <a>Riavvia in modalità provvisoria...</a>
        <hr />
        <a>Partecipa</a>
        <a>Donazione a LibreOffice</a>
        <hr />
        <a>Informazioni sulla licenza</a>
        <a>Controlla aggiornamenti...</a>
        <hr />
        <a>Informazioni su LibreOffice</a>
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
.dropdownAiuto {
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

.dropdownAiuto a {
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

.dropdownAiuto a:hover {
    background-color: #91C9F7;
}
</style>