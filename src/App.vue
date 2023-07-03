<script>
export default {

};
</script>
<template>
  <header></header>
  <main>
    <div class="container">
      <!-- cerchi -->
      <div class="circles d-flex align-items-center py-3">
        <div class="big-circle">
        </div>
        <div class="small-circles d-flex px-2">
          <span class="bg-danger"></span>
          <span class="bg-warning"></span>
          <span class="bg-success"></span>
        </div>
      </div>
      <!-- pokemon list -->
      <div class="row card-container">
        <div class="col">
          <div class="card"></div>
        </div>
      </div>
    </div>
  </main>
  <footer></footer>
</template>
<style lang="scss">
@use './assets/scss//style.scss';
</style>