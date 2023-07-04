<script>
import { colorMap } from '../../data/index';
export default {
    props: {
        name: String,
        image: String,
        number: Number,
        type: String,
    },
    computed: {
        bgColor() {
            return colorMap[this.type];
        }
    }
};
</script>

<template>
    <div class="my-card text-center my-3" :style="`background-color: ${bgColor}`">
        <img :src="image" :alt="name" class="img-fluid rounded-circle my-2">
        <div>{{ number }}</div>
        <h4>{{ name }}</h4>
        <p><em>{{ type }}</em></p>
    </div>
</template>

<style scoped lang="scss">
img {
    height: 100px;
    width: 100px;
}

h4 {
    font-size: 16px;
}

.my-card {
    height: 200px;
    width: 200px;
    border-radius: 20px;
}
</style>