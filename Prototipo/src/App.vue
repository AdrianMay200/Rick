<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Personajes from './components/Personajes.vue'

</script>



<template>
  <header>
    
  </header>
  <div class="headerr">
    <nav class=" bg-gradient-to-r from-blue-300 to-blue-500">
    <div class="max-w-screen-xl px-4 py-3 mx-auto md:px-6">
        <div class="flex items-center">
            <ul class="flex flex-row mt-0 mr-6 space-x-8 text-sm font-medium ">
                <li class="hover:-translate-y-1 hover:scale-110 duration-300 hover:text-cyan-900">
                  <RouterLink to="/">Inicio</RouterLink> 
                </li>
                <li class="hover:-translate-y-1 hover:scale-110 duration-300 hover:text-cyan-900">
                  <RouterLink to="/about">Acerca de</RouterLink>
                    
                </li>
                <li class="hover:-translate-y-1 hover:scale-110 duration-300 hover:text-cyan-900">
                  <RouterLink to="/personajes">Personajes</RouterLink>
                </li>
            </ul>
        </div>
    </div>
</nav>

  </div>
  
<RouterView />

</template>


<style scoped>
  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }

</style>

