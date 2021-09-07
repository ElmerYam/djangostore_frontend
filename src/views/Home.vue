<template>
  <div class="home">
    <section class="hero-body has-text-centered">
      <p class="title mb-6">
        Welcome to DjStore
      </p>
      <p class="subtitle">
        The best Store online
      </p>
    </section>

    <div class="columns is-multiline">
      <div class="column is-12">
        <h2 class="is-size-2 has-text-centered">
          Lates products
        </h2>
      </div>

      <div class="column is-3" v-for="product in latestProducts" v-bind:key="product.id">
        <div class="box">
          <figure class="image mb-4" >
            <img :src="product.get_thumbnail">
          </figure>
          <h3 class="is-size-4">{{ product.name }}</h3>
          <p class="is-size-6 has-text-grey">${{ product.price }}</p>
          View Details
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  data() {
    return {
      latestProducts: [
        {
        "id": 1,
        "name": "Brown leather",
        "get_absolute_url": "/summer/brown-leather/",
        "description": "the desc",
        "price": "199.00",
        "get_image": "http://127.0.0.1:8000/media/uploads/EKS.jpg",
        "get_thumbnail": "http://127.0.0.1:8000/media/uploads/uploads/EKS.jpg"},
        {
          "id": 2,
          "name": "Elmer leather",
          "get_absolute_url": "/summer/brown-leather/",
          "description": "the desc",
          "price": "199000.00",
          "get_image": "http://127.0.0.1:8000/media/uploads/EKS.jpg",
          "get_thumbnail": "http://127.0.0.1:8000/media/uploads/uploads/EKS.jpg"
        },
        {}]
    }
  },
  components: {
    HelloWorld
  }
}
</script>

<style scoped>
  .image{
    margin-top: -1.25 rem;
    margin-left: -1.25 rem;
    margin-right: -1.25 rem;
  }
</style>