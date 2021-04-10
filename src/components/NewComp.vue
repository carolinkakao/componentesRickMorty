<template>
 <div>
   <h1>Imagenes Rick and Morty</h1>
   <button @click=" obtenerDatos()" type="button" class="btn btn-danger">Llamar Personajes</button>
  <div class="container mt-4" v-if="arregloRick.length > 0">
     <div class="row">
       <div class="col-3" v-for="(cicloMorty,index) in arregloRick" :key="index">
   <div class="card" style="width: 18rem;">
  <img :src="cicloMorty.image" class="card-img-top" alt="">
  <div class="card-body">
    <h5>{{cicloMorty.name}}</h5>
    <p class="card-text"></p>
  </div>
   </div>
       </div>
     </div>
</div>
 </div>
</template>

<script>
export default {
  name: "NewComp",
  data (){
   return{
     arregloRick: [],
   };
 },
 methods:{
   async obtenerDatos(){
     const url = "https://rickandmortyapi.com/api/character";
     try {
        const data = await fetch(url);
        const dataJson = await data.json();
        //console.log(dataJson.results);
        this.arregloRick = dataJson.results;
      } catch (error) {
        console.log(error);
      }
   },
   
 }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
