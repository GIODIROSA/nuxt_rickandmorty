<template>
  <div>
    <Navbar />
    <!-- CARD -->
    <div class="container">
      <div class="columns">
        <div
          class="card column"
          v-for="(personaje, index) in personajes"
          :key="index"
        >
          <div class="card-image">
            <figure class="image is-4by3">
              <img :src="personaje.imagen" alt="Placeholder image" />
            </figure>
          </div>
          <div class="card-content">
            <div class="media">
              <div class="media-content">
                <p class="title is-4">{{ personaje.nombre }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- FINAL CARD -->
  </div>
</template>

<script>
import Navbar from '../components/Navbar'

export default {
  name: 'IndexPage',
  data() {
    return {
      personajes: [
        {
          id: 1,
          nombre: 'Morty',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/2.jpeg',
        },
        {
          id: 2,
          nombre: 'Rick',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/1.jpeg',
        },
        {
          id: 3,
          nombre: 'Summer',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/3.jpeg',
        },
        {
          id: 4,
          nombre: 'Beth',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/4.jpeg',
        },
        {
          id: 5,
          nombre: 'Jerry',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/5.jpeg',
        },
      ],
    }
  }, //final de data
  components: {
    Navbar,
  },
}
</script>

<style scoped>
/* .container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
} */

.card {
  margin: 120;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 20px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
