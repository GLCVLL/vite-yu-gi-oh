<script>
export default {
    props: {
        name: String,
        image: String,
        number: Number,
        type: String,
        color: String,
    },
};
</script>

<template>
    <div class="my-card text-center my-3">
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
    background-color: aquamarine;
    border-radius: 20px;
}
</style>