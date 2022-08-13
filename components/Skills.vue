<template>
  <div class="hello">
    <v-row no-gutters>
      <v-col class="mx-1">
        <h1>Vue</h1>

        <form @submit.prevent="addSkill">
          <input
            type="text"
            placeholder="Enter a skill you have"
            v-model="skill"
          />
        </form>

        <ul>
          <li v-for="(data, index) in skills" :key="index" class="py-4">
            {{ data.skill }}
          </li>
        </ul>

        <p>These are the skills that I possess</p>
      </v-col>

      <v-col class="mx-1">
        <h1>Vuetify</h1>

        <v-form @submit.prevent="addSkillVuetify">
          <v-text-field
            label="Enter a skill you have"
            hide-details="auto"
            v-model="skillVuetify"
            outlined
            class="my-5"
          ></v-text-field>
        </v-form>

        <v-list v-for="(data, index) in skills" :key="index">
          <v-card class="py-4"> {{ data.skill }} </v-card>
        </v-list>
        <v-alert type="info" dense>
          These are the skills that I possess
        </v-alert>
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Skills',
  data() {
    return {
      skill: '',
      skillVuetify: '',
      skills: [{ skill: 'Vue.js' }, { skill: 'Vuetify' }],
    }
  },
  methods: {
    addSkill() {
      this.skills.push({ skill: this.skill })
      this.skill = ''
    },
    addSkillVuetify() {
      this.skills.push({ skill: 'vuetify-' + this.skillVuetify })
      this.skillVuetify = ''
    },
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
  font-size: 1.3em;
  background-color: grey;
  border: 5px solid inherit;
  margin-bottom: 2px;
  color: #3e5252;
}

p {
  text-align: center;
  color: gray;
}

.container {
  box-shadow: 0px 0px 40px lightgray;
}

input {
  width: 100%;
  border: 2px solid grey;
  padding: 10px;
  margin: 21px 0px;
  font-size: 1.3em;
  background-color: inherit;
  color: #687f7f;
}
</style>
