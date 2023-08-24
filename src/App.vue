<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Nav from './components/Nav.vue';

</script>

<template>
  <div class="container">
    <Nav/>
  </div>

  <RouterView />
</template>

<style scoped>
.container {
 max-width:1100px;
 margin: 0 auto;
}
</style>
