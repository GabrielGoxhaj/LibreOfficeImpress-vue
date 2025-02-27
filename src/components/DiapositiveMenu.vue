<template>
    <div class="diapositiveMenu">
        <div class="title">
            <p style="font-weight: 500;font-size: 11px;">Diapositive</p>
            <p style="font-size: 16px;">&times;</p>
        </div>
        <div>
            <img class="diapositive" src="../assets/Impress/file_SenzaNome1/menudiapositive.png" />
        </div>
    </div>
</template>

<style scoped>
.diapositiveMenu {
    width: 168px;
    border-right: 1px solid #b0b0b0;
}

.title {
    display: flex;
    justify-content: space-between;
    background-color: #f0f0f0;
    padding-left: 2px;
    align-items: center;
    
}

.title > p {
    border: 1px solid #f0f0f0;
    margin: 0;
    cursor: default;
}

.title > p:nth-child(2) {
    padding-left: 4.5px;
    padding-right: 4.5px;
}

.title > p:nth-child(2):hover {
    background-color: #e4f2fe;
    border: 1px solid #d1eafe;
}

.diapositive {
    border-left: 1px solid #b0b0b0;
    border-top: 1px solid #b0b0b0;
    margin-left: 2px;
}
</style>