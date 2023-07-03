<script>
import CharacterCard from './CharacterCard.vue';
import axios from 'axios';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';
export default {
    components: { CharacterCard },
    data() {
        return {
            characters: {

            }
        }
    },
    created() {
        axios.get(endpoint).then(res => {
            this.characters = res.data.docs
        })
    }
}
</script>

<template>
    <div class="row m-3 bg-secondary row-cols-2 row-cols-ned-3 row-cols-lg-5">
        <div class=" col d-flex justify-content-center" v-for="character in characters" :key="character.id">
            <CharacterCard :name="character.name" :image="character.imageUrl" :number="character.number"
                :type="character.type1" :color="character.color" />
        </div>
    </div>
</template>

<style scoped lang="scss"></style>