<script>
export default {
    data() {
        return {
            title_pptx: 'Il Sistema Solare',
        };
    },
    methods: {
        selectDiapositiva(event) {
            const images = document.querySelectorAll('.diapositivaSelector img');
            images.forEach(img => img.classList.remove('selected'));
            event.target.classList.add('selected');
        },
        getDiapositivaNumber() {
            const images = document.querySelectorAll('.diapositivaSelector img');
            let diapositivaNumber = 0;
            images.forEach((img, index) => {
                if (img.classList.contains('selected')) {
                    diapositivaNumber = index + 1;
                }
            });
            return diapositivaNumber;
        },
        getMaxDiapositivaNumber() {
            const images = document.querySelectorAll('.diapositivaSelector img');
            return images.length;
        }
    }
}
</script>

<template>
    <div class="diapositiveMenu">
        <div class="title">
            <p style="font-weight: 500;font-size: 11px;">Diapositive</p>
            <p style="font-size: 16px;">&times;</p>
        </div>
        <div class="diapositivaSelector">
            <img class="01 selected" @click="selectDiapositiva($event)" src="../../assets/Impress/file_IlSistemaSolare/menu-01.png" />
            <img class="02" @click="selectDiapositiva($event)" src="../../assets/Impress/file_IlSistemaSolare/menu-02.png" />
            <img class="03" @click="selectDiapositiva($event)" src="../../assets/Impress/file_IlSistemaSolare/menu-03.png" />
            <img class="04" @click="selectDiapositiva($event)" src="../../assets/Impress/file_IlSistemaSolare/menu-04.png" />
            <img class="05" @click="selectDiapositiva($event)" src="../../assets/Impress/file_IlSistemaSolare/menu-05.png" />
            <img class="06" @click="selectDiapositiva($event)" src="../../assets/Impress/file_IlSistemaSolare/menu-06.png" />
            <img class="07" @click="selectDiapositiva($event)" src="../../assets/Impress/file_IlSistemaSolare/menu-07.png" />
        </div>
    </div>    
</template>

<style scoped>
.diapositiveMenu {
    width: 168px;
    border-right: 1px solid #b0b0b0;
    max-height: 410px;
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

.diapositivaSelector > img:first-child {
    margin-top: 10px;
}

div > img {
    margin-bottom: 16px;
    padding-bottom: 3px;
    padding-right: 3px;
    padding-top : 3px;
    padding-left: 14px;
    border: 1px solid white;
}

div > img.selected {
    background-color: #90b4d0;
    border: 1px solid #587c98;
}

div > img:hover:not(.selected) {
    background-color: #eaeaea;
    border: 1px solid #b2b2b2;
}

.diapositivaSelector {
    padding-left: 8px;
    border-left: 1px solid #a0a0a0;
    border-top:  1px solid #a0a0a0;
    margin-left: 3px;
    margin-right: 1px;
    max-height: 380px;
    overflow-y: auto;
    background-color: #ffffff;
}
</style>