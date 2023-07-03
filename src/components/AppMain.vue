<script>
import PokemonList from './characters/PokemonList.vue';
export default {
    components: { PokemonList },
};
</script>

<template>
    <main>
        <div class="container">
            <!-- cerchi -->
            <div class="circles d-flex align-items-center py-3 mb-3">
                <div class="big-circle">
                </div>
                <div class="small-circles d-flex px-2">
                    <span class="bg-danger"></span>
                    <span class="bg-warning"></span>
                    <span class="bg-success"></span>
                </div>
            </div>
            <!-- pokemon list -->
            <div class="card-container">
                <PokemonList />
            </div>
        </div>
    </main>
</template>

<style scoped lang="scss"></style>