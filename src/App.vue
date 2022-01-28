<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
      color="green darken-2"
    >
      <Sidebar
      :userName="user_name"
      :links="links"
      />
    </v-navigation-drawer>

    <v-app-bar app
      color="red"
    >
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>PokeDex</v-toolbar-title>
    <AppBar/>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
  import AppBar from '@/layout/AppBar';
  import Sidebar from '@/components/sidebar/sidebar';
  export default {
    components: {
      AppBar,
      Sidebar,
    },
    data () {
      return {
        user_name: 'Ash',
        drawer: null,
        cards: ['Today', 'Yesterday'],
        links: [
          ['mdi-home', 'Home', 'home'],
          ['mdi-compass', 'Explore', 'explore'],
          ['mdi-chart-donut', 'Progress', 'progress'],
          ['mdi-account', 'Settings', 'settings'],
        ],
      };
    },
  }
</script>


<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
