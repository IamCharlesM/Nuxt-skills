<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app>
      
<v-app-bar-nav-icon @click.stop="drawer = !drawer" />

      <v-toolbar-title v-text="title" class=" mx-auto text-center" />
      <v-spacer />

    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer :absolute="!fixed" app>
      <span>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veniam perferendis at qui velit itaque voluptas harum facere nostrum ipsa dignissimos deleniti asperiores, provident veritatis ex, quae eius saepe repellat eaque?</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-home',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-information-outline',
          title: 'Description',
          to: '/description',
        },
        {
          icon: 'mdi-account',
          title: 'About Me',
          to: '/about',
        },
      ],
      miniVariant: false,
      title: 'General Skills',
    }
  },
}
</script>
