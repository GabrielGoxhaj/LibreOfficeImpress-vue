<script>
import menu01 from "../../assets/Impress/file_SenzaNome1/menu-01.png";

export default {
    data() {
        return {
            images: [
                { src: menu01, selected: true },
        ],
        title_pptx: 'Senza Nome 1.pptx',
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
    height: 380px;
    overflow-y: auto;
    background-color: #ffffff;
}
</style>