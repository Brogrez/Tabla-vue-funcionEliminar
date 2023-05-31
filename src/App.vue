<template>
  <div id="app">
    <Tabla :juegos="games" @eliminar="eliminarJuego" />
  </div>
</template>

<script>
import Tabla from './components/Tabla.vue'


export default {
  name: 'App',
  components: { 
    Tabla
  },
  data(){
    return {
      games: ["Arena of valor", "Pokemon Unite", "Donkey Kong", "Heroes of the storm", "Valorant"]
    }  
  },
  methods:{
    eliminarJuego(id){
      const juegosRestantes = this.games.filter((game,index) => index !== id) 
      this.games = juegosRestantes
    }
  }
}
</script>

