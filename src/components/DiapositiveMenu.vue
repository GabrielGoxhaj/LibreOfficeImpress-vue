<template>
    <div class="diapositiveMenu">
        <div class="title">
            <p>Diapositive</p>
            <p>&times;</p>
        </div>
        <div>
            <img class="diapositive" src="../assets/Impress/diapositive_menu/vuoto.png" />
        </div>
    </div>
</template>

<style scoped>
.diapositiveMenu {
    width: 168px;
    border-right: 1px solid #b0b0b0;
    border-bottom: 1px solid #b0b0b0;
}

.title {
    display: flex;
    justify-content: space-between;
    background-color: #f0f0f0;
    padding: 4px;
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