<template>
  <div class="hello">
    <v-row no-gutters>
      <v-col>
        <v-card>
          {{ name }}
        </v-card>
      </v-col>
    </v-row>

    <v-row no-gutters>
      <v-col>
        <h1>Default Button</h1>
        <button v-on:click="changeName" v-bind:disable="btnState" class="default-button">
          Change name
        </button>
        
        {{ btnState ? 'The button is disabled' : 'The button is active'}}

        </v-col
      >
      <v-col>
        <h1>Vuetify Button</h1>
        <v-btn depressed small color="primary" disabled>text</v-btn></v-col
      >
    </v-row>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Skills',
  data() {
    return {
      name: 'General Skills',
      btnState: true,
    }
  },
}
</script>

<style>
.default-button {
  border-radius: 5%;
  background-color: red;
  padding: 0.2em
  }
</style>
