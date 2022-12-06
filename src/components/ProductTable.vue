<template>
    <div class="col-5 my-5 mx-5">
  <table class="table text-warning">
  <thead>
    <tr>
      <th scope="col">Imagen</th>
      <th scope="col">Nombre</th>
      <th scope="col">Precio</th>
      <th scope="col">Stock</th>
    </tr>
  </thead>
  <tbody>
    <tr  v-for="(producto, index) of productos" :key="index">
      <td><img class="rounded w-20 h-20" :src="producto.imagen"/></td>
      <td><p>{{producto.titulo}}</p></td>
      <td><p>{{producto.costo}}</p></td>
      <td><p>{{producto.stock}}</p></td>
    </tr>
  </tbody>
</table>
</div>
</template>

<script>
export default {
  name: "ProductTable",
  props: {
    productos: Array,
    bg1: String,
    bg2: String,
    text: String,
    text2: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
