<template>
  <div class="hello">
    <v-row no-gutters>
      <v-col>
        <h1>Vue</h1>
        <ul>
          <li v-for="(data, index) in skills" :key="index">
            {{ data.skill }}
          </li>
        </ul>

        <p>These are the skills that you possess</p>
      </v-col>

      <v-col>
        <h1>Vuetify</h1>
        <v-list v-for="(data, index) in skills" :key="index">
          <v-card class="py-5"> {{ data.skill }} </v-card>
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
      showAlert: true,
    }
  },
}
</script>

<style scoped>
ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

ul li {
  padding: 20px;
  font-size: 1.3em;
  background-color: grey;
  border: 5px solid inherit;
  margin-bottom: 2px;
  color: #3e5252;
}

p {
  text-align: center;
  padding: 30px 0;
  color: gray;
}

.container {
  box-shadow: 0px 0px 40px lightgray;
}
</style>
