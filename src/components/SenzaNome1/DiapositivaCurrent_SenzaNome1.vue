<template>
    <div>
        <img :src="currentImage.src" v-if="currentImage" />
    </div>
</template>

<script>
import diapositiva01 from "../../assets/Impress/file_SenzaNome1/diapositiva-01.png";

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
            ]
        };
    },
    computed: {
        currentImage() {
            return this.images[this.diapositivaNumber - 1];
        }
    }
}
</script>

<style scoped>
img {
    max-width: 100%;
    max-height: 100%;
}
</style>