<script>
export default {
    data() {

        return {
            image: "01.jpg"
        }
    },
    methods: {
        getImagePath: function (imagePath) {
            return new URL(imagePath, import.meta.url).href;
        }
    }
}
</script>
<template>
    <div class="box-img">
        <img :src="getImagePath(`../assets/img/${this.image}`)">
    </div>
</template>
<style scoped>
.class {
    height: 150px;
}

img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>