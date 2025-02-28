<template>
    <div class="menuLaterale">
        <button><img src="../assets/Impress/icons/icons_menu_laterale/impostazioni.png"></button>
        <button><img src="../assets/Impress/icons/icons_menu_laterale/proprietà.png"></button>
        <button><img src="../assets/Impress/icons/icons_menu_laterale/galleria.png"></button>
        <button><img src="../assets/Impress/icons/icons_menu_laterale/navigatore.png"></button>
        <button><img src="../assets/Impress/icons/icons_menu_laterale/forme.png" ></button>
        <button><img src="../assets/Impress/icons/icons_menu_laterale/cambio-diapositiva.png"></button>
        <button><img src="../assets/Impress/icons/icons_menu_laterale/animazione.png"></button>
        <button><img src="../assets/Impress/icons/icons_menu_laterale/diapositive-schema.png"></button>
    </div>
</template>

<style scoped>
.menuLaterale {
    display: flex;
    flex-direction: column;
    border-left: 1px solid #b0b0b0;
}

button {
    border: 1px solid #f0f0f0;
    background-color: #f0f0f0;
    padding: 4px;
    margin: 2px;
}

button:hover {
    background-color: #e4f2fe;
    border: 1px solid #d1eafe;
}
</style>