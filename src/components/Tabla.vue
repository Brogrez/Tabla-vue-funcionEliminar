<template>
  <div class="container mt-5">
    <table class="table w-50 mx-auto text-center">
  <thead>
    <tr class="table-dark">
      <th scope="col">#</th>
      <th scope="col">Juegos</th>
      <th scope="col">Eliminar Juego de tu lista</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="(juego, index) in juegos" :key="index" class="table-dark table-active">
        <td>{{index+1}}</td>
        <td>{{juego}}</td>
        <td><button @click="eliminarJuego(index)" type="button" class="btn btn-danger">Eliminar</button></td>
    </tr>
  </tbody>
</table>
  </div>
</template>

<script>
export default {
    props: {
        juegos:Array,
    },
    methods: {
        eliminarJuego(id){
            this.$emit('eliminar', id)
        }
  }
}
</script>

<style>

</style>