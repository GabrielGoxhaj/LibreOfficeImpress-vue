<template>
    <div id="dropdownDocumentiRecenti" class="dropdownDocumentiRecenti" :style="style">
        <a @click="$emit('update-title', 'Il Sistema Solare')"><div><img src="../../../assets/Impress/icons/icons_dropdown/file/file-presentazione.png"> <u>1</u>. Il Sistema Solare.pptx</div></a>
        <a><div><img src="../../../assets/Impress/icons/icons_dropdown/file/file-presentazione.png"> <u>2</u>. IVA.pptx</div></a>
        <a><div><img src="../../../assets/Impress/icons/icons_dropdown/file/file-presentazione.png"> <u>3</u>. Social Media Marketing.pptx</div></a>
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
.dropdownDocumentiRecenti {
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

.dropdownDocumentiRecenti a {
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

.dropdownDocumentiRecenti a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownDocumentiRecenti a div img {
    margin-right: 5px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownDocumentiRecenti a:hover {
    background-color: #91C9F7;
}

hr {
    margin: 0;
    color: #d7d7d7;
}
</style>