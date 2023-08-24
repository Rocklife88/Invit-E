<script setup>
import { ref } from 'vue'

const inputName = ref('');
const nameList = ref([])

// const addName = () => {
//   if (inputName.value !== '') {
//     nameList.value.push(inputName.value)
//     inputName.value = '';
//   } else {
//     alert('you need to insert your name here')
//   }
// }

const addName = () => {
  if (inputName.value !== '') {
    nameList.value.unshift(inputName.value); 
    inputName.value = '';
  } else {
    alert('Devi inserire un nome');
  }
};

const refreshList= ()=> {
  nameList.value=[]
  inputName.value=''
}
</script>

<template>
  <div class="container">
    <div class="div">
      <input v-model.trim="inputName" type="text" placeholder="Add invitee to the list...">
    </div>
    <div class="button-wrapper">
      <button @click="addName" >Add Name To The List</button>
      <button @click="refreshList">Delete List</button>
    </div>
    <div class="list-container">
      <ul class="name-list">
        <TransitionGroup name="invitees">
          <li v-for="(name, index) in nameList" :key="index" >{{name}}</li>
          <li>Luigi Loviso</li>
          <li>Luisa Hall</li>
      </TransitionGroup>
      </ul>
    </div>
  </div>
  </template>

<style scoped>
.container {
  max-width: 1100px;
  margin: 0 auto;
  margin-top: 3rem;
  padding: 0.8rem 1rem;
  text-align:center;
}

input[type="text"] {
  width: 400px; 
  padding: 1.5rem 2rem 1.5rem 1rem;
  font-size: 1rem;
  border-radius: 5px;
  border: none;
  text-align: left;
  margin-bottom:1.4rem;
}
button {
  width:400px;
  padding: 1.4rem 7rem ;
  text-align: center;
  border-radius: 0.5rem;
  border: none;
  background-color: aqua;
  color: rgb(7, 83, 83);
  font-size: 1rem;
  font-weight: 600;
}

li{
  width:400px;
  border:1px solid aqua;
  padding:1rem;
  border-radius:5px;
}

.button-wrapper{
  display:flex;
  flex-direction:column;
  align-items:center;
  justify-content: center;
  gap:0.8rem;
}
.list-container {
  margin-top: 2rem;
  margin: 3rem auto;
  display: flex;
  flex-direction: column;
  align-items: center; 
  justify-content: center;
  width:500px;
  text-align: left; 
}

.name-list {
  list-style: none;
  padding: 0; 
  margin: 0;
}

.name-list li {
  margin-bottom: 0.5rem; 
  font-size:1.4rem;
  font-weight:600px;
}

.invitees-enter-from{
opacity:0;
transform:scale(0.5);
}


.invitees-enter-active{
transition: all 0.6s ease;
}


  
  .invitees-leave-to{
    opacity:0;
    transform:scale(0.5);
  }
  
  
  .invitees-leave-active{
  transition: all 0.6s ease;
  position:absolute;
  }

.invitees-move{
  transition: 0.6s ease all;
}





@media (max-width: 767px) {
  input[type="text"] {
    width: 310px; 
    padding: 1.5rem 2rem 1.5rem 1rem;
    font-size: 1rem;
    border-radius: 5px;
    border: none;
    text-align: left;
    margin-bottom:1.4rem;
  }

  .container{
    max-width:600px;
  }

  button {
    width:310px;
    padding: 1.3rem 4rem ;
    text-align: center;
    border-radius: 0.5rem;
    border: none;
    background-color: aqua;
    color: rgb(7, 83, 83);
    font-size: 1rem;
    font-weight: 600;
  }
  
  li{
    width:310px;
    border:1px solid aqua;
    padding:1rem;
    border-radius:5px;
  }

  .list-container {
    margin-top: 2rem;
    margin: 3rem auto;
    display: flex;
    flex-direction: column;
    align-items: center; 
    justify-content: center;
    max-width:350px;
    text-align: left; 
  }
  

}


</style>
