<script>
export default {
    props: {
        name: String,
        image: String,
        number: Number,
        type: String,
        color: String,
    },
    computed: {
        cardColor() {
            return this.color;
        }
    }
};
</script>

<template>
    <div class="my-card text-center my-3" :class="cardColor">
        <img :src="image" :alt="name" class="img-fluid rounded-circle">
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

.my-card {
    height: 200px;
    width: 200px;
}

.my-card.red {
    background-color: red;
}

.my-card.green {
    background-color: green;
}

.my-card.blue {
    background-color: skyblue;
}
</style>