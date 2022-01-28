<template>
  <div>
      <v-sheet
        color="grey lighten-4"
        class="pa-4"
      >
        <v-avatar
          class="mb-4"
          color="grey darken-1"
          size="64"
        ></v-avatar>

        <div>{{userName}}</div>
      </v-sheet>

      <v-divider></v-divider>

      <v-list>
        <v-list-item
          v-for="[icon, text, route ] in links"
          :key="icon"
          link
          @click="jumpTab(route)"
        >
          <v-list-item-icon>
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
  </div>
</template>

<script>
export default {
    name: 'Sidebar',
    props: {
        links: {
            type: Array,
            default() {
                return [];
            },
        },
        userName: {
            type: String,
            default() {
                return 'NA';
            },
        },
    },
    methods: {
        jumpTab(route) {
            console.log(route);
            // if (route) {
                this.$router.push({ path: route })
            // }
        }
    }
}
</script>

<style>

</style>