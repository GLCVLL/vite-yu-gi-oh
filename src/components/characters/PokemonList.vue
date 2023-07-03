<script>
import CharacterCard from './CharacterCard.vue';
import { store } from '../../data/store';

export default {
    components: { CharacterCard },
    data() {
        return { store: store }
    },
}
</script>

<template>
    <div class="row m-3 bg-secondary row-cols-2 row-cols-ned-3 row-cols-lg-5">
        <div class=" col d-flex justify-content-center" v-for="character in store.characters" :key="character.id">
            <CharacterCard :name="character.name" :image="character.imageUrl" :number="character.number"
                :type="character.type1" :color="character.color" />
        </div>
    </div>
</template>

<style scoped lang="scss"></style>