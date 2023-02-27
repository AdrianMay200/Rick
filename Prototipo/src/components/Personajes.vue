<script>
import axios from 'axios'
let API_URL = `https://rickandmortyapi.com/api/character`
export default {
  data() {
    return {
      info: [],
      personajes: [],
      pagina:1,
      siguiente:null,
      anterior:null,
      buscar:'',
    }
  },
  mounted() {
    axios.get(API_URL)
      .then((response) => {
        this.info = response.data.info;
        this.personajes = response.data.results;
      })
  },
  
  methods: {
    navpag(num) {
      API_URL='https://rickandmortyapi.com/api/character/?page='+this.pagina
      console.log(API_URL)
      axios.get(API_URL)
      .then((response) => {
        console.log(response.config)
        this.info = response.data.info;
        this.personajes = response.data.results;
      })
    },
    buscador(text) {
      API_URL='https://rickandmortyapi.com/api/character/?'+('name='+text ||'&status='+text)
      console.log(API_URL)
      axios.get(API_URL)
      .then((response) => {
        console.log(response.config)
        this.info = response.data.info;
        this.personajes = response.data.results;
      })
    },
  },
}

</script>

<template >
  <div class="text-center" >
    <input v-model="buscar" placeholder="Buscar" style="margin: 10px 10px 10px 10px" class="leading-tight text-blue-700 border border-blue focus:outline-none focus:shadow-outline shadow appearance-none border rounded" />
  <button @click="buscador(buscar) " class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Buscar</button>

  <h2 style="margin: 100px 10px 10px 10px">Hay {{ info.count }} personajes en el programa de Rick & Morty</h2>

  <div class="inline-flex" >



  </div>

  <button class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded-l" v-if="pagina!==1" @click="navpag(pagina--)">Anterior</button>
  
  <a>{{pagina }}</a>
  <button class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded-r" v-if="pagina!==this.info.pages" @click="navpag(pagina++)">Siguiente</button>
  
  
  <ul>
  
    <li v-for="d in personajes">
    <div  style="margin: 100px 10px 10px 10px">
      <a class="text-xl info" style="margin: 10px 10px 10px 10px"><b>{{ d.name }}</b></a> 
      
      <br>
      <div class="textoimagen">

      <img v-bind:src=" d.image " alt="Personajes_Rick_Morty" class="imgRedonda">

      <div class="informacion" style="margin: 10px 10px 10px 10px">
        <a class="text-xl">id-{{ d.id }}</a>
       
      <a class="text-xl info" style="margin: 10px 10px 10px 10px">Género: {{ d.gender }}</a>
      <a class="text-xl info" style="margin: 10px 10px 10px 10px">Especie: {{ d.species }}</a>
      <a class="text-xl info" style="margin: 10px 10px 10px 10px">Estado: {{ d.status }}</a>
      </div>
      </div>
    </div>
    </li>
 
  </ul>
  </div>
</template>

<style>
   .boton{
    padding: 5px;
    border-radius:50%;
   }

  .textoimagen{
    display: inline-flex;
  }
  .info{
    display: block;
  }
  .informacion{
    float: right;
  }
  .caja{
    display: inline;
  }
  .box{
    padding: 20px;
  }
  .imgRedonda {
    width:300px;
    height:300px;
    border-radius:150px;
}

  
</style>