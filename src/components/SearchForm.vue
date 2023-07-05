<script>
export default {
    data() {
        return {
            types: [
                "Bug",
                "Dark",
                "Dragon",
                "Electric",
                "Fairy",
                "Fighting",
                "Fire",
                "Flying",
                "Ghost",
                "Grass",
                "Ground",
                "Ice",
                "Normal",
                "Poison",
                "Psychic",
                "Rock",
                "Steel",
                "Water"
            ]
        }
    },
    emits: ['type-selected'],
}
</script>

<template>
    <div class="container container-select">
        <select class="form-select form-select-sm" style="width: 300px" v-model="typeFilter"
            @change="$emit('type-selected', typeFilter)">
            <option selected>Scegli il tipo...</option>
            <option v-for="type in types" :key="type">{{ type }}</option>
        </select>
    </div>
</template>