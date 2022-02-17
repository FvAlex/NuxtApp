<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
        <v-card-title class="headline">
          Welcome to the Fat World
        </v-card-title>
        <v-card-text>
          <p>You can find all the post and the comment of the Fat Man and Fat Woman.</p>
          <p>
            For more information on Fat World, check our <a
              href="https://www.mcdonalds.fr/"
              target="_blank"
              rel="noopener noreferrer"
            >
              documentation
            </a>.
          </p>
          <p>
            If you have questions, please join the official <a
              href="https://www.quick.fr/"
              target="_blank"
              rel="noopener noreferrer"
              title="chat"
            >
              site
            </a>.
          </p>
          <p>
            Find a bug? Report it on the <a
              href="https://sante.lefigaro.fr/mieux-etre/nutrition-aliments/fruits-legumes/quest-ce-que-cest"
              target="_blank"
              rel="noopener noreferrer"
              title="contribute"
            >
              site report
            </a>.
          </p>
          <p>Thank you for making us a better world.</p>
          <div class="text-xs-right">
            <em><small>&mdash; Alexandre Fievez</small></em>
          </div>
          <hr class="my-3">
          <a
            href="https://www.mcdonalds.fr/"
            target="_blank"
            rel="noopener noreferrer"
          >
            Documentation
          </a>
          <br>
          <a
            href="https://github.com/mcdcorp"
            target="_blank"
            rel="noopener noreferrer"
          >
            GitHub
          </a>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
