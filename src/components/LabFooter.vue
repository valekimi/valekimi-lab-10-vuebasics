<script setup>
import { ref, reactive } from 'vue'

const author = reactive({
  name: 'John Doe',
  books: ['Vue 2 - Advanced Guide', 'Vue 3 - Basic Guide', 'Vue 4 - The Mystery']
})

const isShown = ref(true)

const cityList = ref([
  {
    name: 'Barcelona',
    description: 'city',
    content: 'beautiful',
    img: "https://www.spain.info/.content/imagenes/cabeceras-grandes/cataluna/park-guell-barcelona-s-305364611.jpg"
  },
  {
    name: 'NY',
    description: 'city',
    content: 'fancy',
    img: "https://i.natgeofe.com/k/5b396b5e-59e7-43a6-9448-708125549aa1/new-york-statue-of-liberty_2x1.jpg"
  },
  {
    name: 'Rome',
    description: 'city',
    content: 'big',
    img: "https://media.timeout.com/images/105212586/750/562/image.jpg"
  },
  {
    name: 'Malaga',
    description: 'city',
    content: 'nice',
    img: "https://upload.wikimedia.org/wikipedia/commons/4/40/M%C3%A1laga_-_vistas_desde_el_Parador_de_Gibralfaro_01_%28cropped%29.jpg"
  }
])

function show() {
  return author.name + ' Chimento'
}
</script>



<template>
  <section>
    <h1>I am the Footer</h1>
    <p>{{ 2 + 2 }}</p>
    <p>{{ show() }}</p>
    <p v-show="isShown">Este parrafo se oculta</p>
    <br />
    <ul>
      <li v-for="city in cityList" :key="city">
        <p>{{ city.name }}</p>
        <p>{{ city.descripcion }}</p>
        <p>{{ city.content }}</p>
        <img :src="city.img" alt="" />
      </li>
    </ul>

    <button></button>
  </section>
</template>



<style scoped>

img {
  width: 200px;
  height: 70px;
}

</style>
