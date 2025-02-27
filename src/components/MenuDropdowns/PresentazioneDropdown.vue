<template>
    <div id="dropdownPresentazione" class="dropdownPresentazione" :style="style">
        <a>Inizia dalla prima diapositiva</a>
        <a>Inizia dalla diapositiva corrente</a>
        <hr />
        <a>Presentazione cronometrata</a>
        <a>Presentazione personalizzata...</a>
        <hr />
        <a>Impostazioni presentazione...</a>
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
.dropdownPresentazione {
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

.dropdownPresentazione a {
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

.dropdownPresentazione a:hover {
    background-color: #91C9F7;
}
</style>