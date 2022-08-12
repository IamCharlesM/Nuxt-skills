<template>
  <v-row>
    <v-col class="text-center">
      <Skills />
    </v-col>
  </v-row>
</template>

<script>
import Skills from '~/components/Skills.vue';
export default {
    name: "index",
    components: { Skills }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,700');

body {
  font-family: 'Montserrat', sans-serif;
}
</style>
