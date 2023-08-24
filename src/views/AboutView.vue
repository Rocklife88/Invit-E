<template>
  <div class="about">
    <h2>About This App</h2>
    <p>
      This simple Vue.js app allows you to create a list of invitees. You can add names to the list and watch them appear with a smooth animation. 
      The most recent name you add will always be shown at the top of the list.
    </p>
    <p>
      To get started, just type a name in the input field and click the "Add Name" button. 
      The name will be added to the top of the list, and any existing names will smoothly shift downwards to make room for the new name. You can also clear the entire list by clicking the "Clear List" button.
    </p>
    <p>
      The app uses Vue's reactivity system to manage the list of names and provides a visually pleasing user experience with smooth animations.
    </p>
  </div>
</template>

<script setup>

</script>

<style scoped>
.about {
  max-width: 1100px;
  margin: 0 auto;
  padding:0 1.4rem;


}

h2 {
  font-size: 1.8rem;
  margin-bottom: 1rem;
  color:aqua;
}

p {
  font-size: 1.2rem;
  margin-bottom: 1.5rem;
  line-height:1.8;
  font-size:1.1rem;
  
}
</style>
