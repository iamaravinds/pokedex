<template>
  <v-container>
    <v-row>
      <v-col
        v-for="(pokemon, index) in pokemons"
        :key="index"
        cols="4"
      >
      <Card
        :pokemon="pokemon"
      />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  import Card from '@/components/cards/card';
  import pokemons from '@/services/api-factory'
  export default {
    name: 'Home',
    components: {
      Card,
    },
    data: () => ({
      pokemons,
    }),
  }
</script>
