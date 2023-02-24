<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Personajes from './components/Personajes.vue'

</script>

<template>

 

  <header>

    <div>


      <nav>
        <RouterLink to="/">Home</RouterLink> 
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/personajes">Personajes</RouterLink>
      </nav>
    </div>
  </header>
  

  <RouterView />
</template>


