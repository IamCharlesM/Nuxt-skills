<template>
  <div class="hello">
    <v-row no-gutters>
      <v-col>
        <h1>Vue</h1>
        <ul>
          <li v-for="(data, index) in skills" :key="index">
            {{ index }}. {{ data.skill }}
          </li>
        </ul>
      </v-col>

      <v-col>
        <h1>Vuetify</h1>
        <v-list v-for="(data, index) in skills" :key="index"> 
        <v-card>
            {{ index}}. {{ data.skill}}
        </v-card>
        </v-list>
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Skills',
  data() {
    return {
      skills: [{ skill: 'Vue.js' }, { skill: 'Vuetify' }],
    }
  },
}
</script>

<style>
.default-button {
  border-radius: 5%;
  background-color: red;
  padding: 0.2em;
}
</style>
