<template>
  <v-layout>
    <v-flex class="my-article">
      <img
        src="/v.png"
        alt="Vuetify.js"
        class="mb-5"
      >

      <v-card color="#02012E">
        <v-card-title class="headline">
          Viblo Platform
        </v-card-title>

        <v-card-subtitle>
          The introduction below is quoted from <a href="https://about.viblo.asia">https://about.viblo.asia</a>
        </v-card-subtitle>

        <v-card-text v-html="htmlContents" />
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'
import htmlContents from '@/contents/article'

@Component
export default class Inspire extends Vue {
  get htmlContents (): string {
    return htmlContents
  }
}
</script>

<style lang="scss">
  .my-article {
    .about-text {
      &, a {
        color: #449fdc;
      }
    }
  }
</style>
