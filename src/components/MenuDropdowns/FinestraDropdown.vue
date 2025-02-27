<template>
    <div id="dropdownFinestra" class="dropdownFinestra" :style="style">
        <a >Nuova finestra</a>
        <a>Chiudi finestra</a>
        <hr />
        <a >Senza nome 1 - LibreOffice Impress</a>
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
.dropdownFinestra {
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

.dropdownFinestra a {
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

.dropdownFinestra a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownFinestra a div img {
    margin-right: 5px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownFinestra a:hover {
    background-color: #91C9F7;
}

hr {
    margin: 0;
    color: #d7d7d7;
}
</style>