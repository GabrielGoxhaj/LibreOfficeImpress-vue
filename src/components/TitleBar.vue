<template>
    <div class="titleBar">
        <div class="title">
            <img src="../assets/Impress/icon-libreofficeimpress.png" />
            <span> Senza nome 1 -- LibreOffice Impress</span>
        </div>
        <div class="buttons">
            <div class="restore" id="impressRestore"><img src="../assets/Impress/icon-restore.svg" /></div>
            <div class="close" id="impressClose">&times;</div>
        </div>
    </div>
</template>

<style scoped>
.title {
    margin-left: 5px;
    display: flex;
    align-items: center;
}

.title>span {
    font-size: 15px;
    margin-left: 6px;
}

.titleBar {
    align-items: center;
    background-color: #fdfdfd;
}

.titleBar,
.buttons {
    display: flex;
    justify-content: space-between;
}

.restore:hover {
    background: #e5e5e5;
}

.close:hover {
    background: red;
    color: white;
}

.restore {
    display: inline;
    float: right;
    width: 60px;
    height: 30px;
    font-size: 20px;
    font-family: 'Times New Roman', Times, serif;
    margin: auto auto;
    text-align: center;
    transition: 0.2s;
}

.close {
    display: inline;
    float: right;
    width: 60px;
    height: 30px;
    font-size: 25px;
    font-family: 'Times New Roman', Times, serif;
    margin: auto auto;
    text-align: center;
    transition: 0.2s;
}
</style>