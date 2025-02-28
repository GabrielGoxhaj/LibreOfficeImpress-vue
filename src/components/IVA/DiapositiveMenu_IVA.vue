<script>
import menu01 from "../../assets/Impress/file_IVA/menu-01.png";
import menu02 from "../../assets/Impress/file_IVA/menu-02.png";
import menu03 from "../../assets/Impress/file_IVA/menu-03.png";
import menu04 from "../../assets/Impress/file_IVA/menu-04.png";
import menu05 from "../../assets/Impress/file_IVA/menu-05.png";
import menu06 from "../../assets/Impress/file_IVA/menu-06.png";
import menu07 from "../../assets/Impress/file_IVA/menu-07.png";
import menu08 from "../../assets/Impress/file_IVA/menu-08.png";
import menu09 from "../../assets/Impress/file_IVA/menu-09.png";
import menu10 from "../../assets/Impress/file_IVA/menu-10.png";

export default {
    data() {
        return {
            images: [
                { src: menu01, selected: true },
                { src: menu02, selected: false },
                { src: menu03, selected: false },
                { src: menu04, selected: false },
                { src: menu05, selected: false },
                { src: menu06, selected: false },
                { src: menu07, selected: false },
                { src: menu08, selected: false },
                { src: menu09, selected: false },
                { src: menu10, selected: false },

            ],
            title_pptx: 'IVA.pptx',
        };
    },
    methods: {
        selectDiapositiva(index) {
            this.images.forEach((img, i) => {
                img.selected = i === index;
            });
            this.$emit('update-diapositiva', index + 1);
        }
    },
    mounted() {
        this.$emit('update-max-diapositiva', this.images.length);
        this.$emit('update-title', this.title_pptx);
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
            <img v-for="(image, index) in images" :key="index" :class="{ selected: image.selected }" @click="selectDiapositiva(index)" :src="image.src" />
        </div>
    </div>    
</template>

<style scoped>
.diapositiveMenu {
    width: 168px;
    border-right: 1px solid #b0b0b0;
    height: 410px;
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

.diapositivaSelector>img:last-child {
    padding-left: -7px;
}
</style>