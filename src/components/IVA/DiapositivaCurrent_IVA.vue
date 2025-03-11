<template>
    <div>
        <img :src="currentImage.src" v-if="currentImage" />
    </div>
</template>

<script>
// import diapositiva01 from "../../assets/Impress/file_IVA/diapositiva-01.png";
// import diapositiva02 from "../../assets/Impress/file_IVA/diapositiva-02.png";
// import diapositiva03 from "../../assets/Impress/file_IVA/diapositiva-03.png";
// import diapositiva04 from "../../assets/Impress/file_IVA/diapositiva-04.png";
// import diapositiva05 from "../../assets/Impress/file_IVA/diapositiva-05.png";
// import diapositiva06 from "../../assets/Impress/file_IVA/diapositiva-06.png";
// import diapositiva07 from "../../assets/Impress/file_IVA/diapositiva-07.png";

export default {
    props: {
        diapositivaNumber: {
            type: Number,
            required: true
        }
    },
    data() {
        return {
            images: [
                { src: diapositiva01 },
                { src: diapositiva02 },
                { src: diapositiva03 },
                { src: diapositiva04 },
                { src: diapositiva05 },
                { src: diapositiva06 },
                { src: diapositiva07 },
            ],
        };
    },
    computed: {
        currentImage() {
            return this.images[this.diapositivaNumber - 1];
        }
    },
}
</script>

<style scoped>
img {
    max-width: 100%;
    max-height: 100%;
}
</style>