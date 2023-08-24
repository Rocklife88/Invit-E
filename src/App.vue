<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Nav from './components/Nav.vue';

</script>

<template>
  <div class="container">
    <Nav/>
  </div>

  <Transition name="route">
    <RouterView />
  </Transition>

</template>

<style scoped>
.container {
 max-width:1100px;
 margin: 0 auto;
}

.route-enter-from{
  opacity:0;
  transform: translateX(200px);
}

.route-enter-to{
  opacity:1;
  transform: translateX(0);
}

.route-enter-active{
transition: all 0.7s ease;
}
</style>
