<template>
  <div>
    <h1>Liste des posts :</h1>
    <button @click="Counter">
      Clique : {{ counter }}
    </button>
    <div v-for="post in pagePosts" :key="post.id">
      <ul>
        <li>
          <h2>{{ post.id }}</h2>
        </li>
        <li>
          <h3>{{ post.title }}</h3>
        </li>
        <li>
          <p>{{ post.body }}</p>
        </li>
      </ul>
      <v-car-actions>
        <v-btn nuxt :to="`/posts/${post.id}`">
          Ouvrir
        </v-btn>
      </v-car-actions>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $axios }) {
    const pagePosts = await $axios.$get('https://jsonplaceholder.typicode.com/posts')

    return { pagePosts }
  },
  data () {
    return {
      counter: 0
    }
  },
  methods: {
    Counter () {
      this.counter++
    }
  }
}
</script>

<style>

</style>
