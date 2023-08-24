<template>
    <header class="container">
      <div class="nav-wrapper">
        <div class="logo">
          Invit-E
        </div>
        <div class="link-wrapper">
          <RouterLink class="nav-links" to="/">Home</RouterLink>
          <RouterLink class="nav-links" to="/about">About</RouterLink>
        </div>
      </div>
    </header>
  </template>
  
  <style scoped>
  .nav-wrapper {
    display: flex;
    height: 4rem;
    padding: 0.7rem;
    align-items: center;
    justify-content: space-between;
  }
  
  .container {
    margin: 0 auto;
    max-width: 1100px;
    padding: 0.8rem 1rem;
  }
  
  .nav-links {
    color: aqua;
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: 500;
    transition: color 0.4s;
    text-align: center; 
  }
  
  .logo {
    font-size: 1.3rem;
    font-weight: 600;
  }
  
  .nav-links:hover {
    color: rgb(85, 227, 232);

  }
  .link-wrapper {
    display: flex;
    gap: 1rem;
    justify-content: flex-end;
  }
  </style>
  