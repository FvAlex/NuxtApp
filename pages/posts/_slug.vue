<template>
  <div>
    <h1>{{ title }}</h1>
    <p>{{ body }}</p>
    <button @click="Counter">
      Clique : {{ counter }}
    </button>
    <h2>Comments: </h2>
    <v-container>
      <v-row>
        <v-col v-for="comment in comments" :key="comment.id" cols="4">
          <v-card>
            <v-card-title>Nom: {{ comment.name }}</v-card-title>
            <v-card-text>Email: {{ comment.email }} <br> Commentaire: {{ comment.body }}</v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <nuxt-link :to="`/posts/${id + 1}`">
      Suivant -->
    </nuxt-link>
    <br>
  </div>
</template>

<script>
export default {
  async asyncData ({ params, $axios }) {
    const slug = params.slug

    const { title, body, id } = await $axios.$get(`https://jsonplaceholder.typicode.com/posts/${slug}`)
    const comments = await $axios.$get(`https://jsonplaceholder.typicode.com/posts/${slug}/comments`)

    return { title, body, slug, id, comments }
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
