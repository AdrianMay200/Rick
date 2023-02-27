<script setup>
import Personajes from "../components/Personajes.vue";
</script>

<template>
  <main class="fondo2">
    <div >
      <h1 class="text-purple-600 text-2xl text-center font-serif">Personajes del programa</h1>

      <Personajes />
    </div>
  </main>
  
</template>

<style>
.fondo2
{
  /*background: radial-gradient(circle, rgba(63,199,251,1) 0%, rgba(62,246,220,1) 5%, rgba(61,241,209,1) 11%, rgba(52,187,206,1) 16%, rgba(23,93,75,1) 38%, rgba(34,111,136,1) 53%, rgba(54,201,190,1) 61%, rgba(26,98,102,1) 63%, rgba(17,68,51,1) 77%, rgba(15,61,51,1) 83%, rgba(12,51,38,1) 86%, rgba(9,38,38,1) 94%, rgba(0,0,0,1) 98%);*/
  background: radial-gradient(circle, rgba(50,176,224,1) 0%, rgba(62,246,238,1) 5%, rgba(61,241,209,1) 11%, rgba(52,187,206,1) 16%, rgba(95,231,225,1) 38%, rgba(34,111,136,1) 53%, rgba(54,201,190,1) 61%, rgba(42,159,166,1) 63%, rgba(67,231,255,1) 71%, rgba(130,255,254,1) 81%, rgba(68,194,204,1) 86%, rgba(44,143,137,1) 94%, rgba(124,205,245,1) 100%);
  width: 100%;
  ;
}



</style>
