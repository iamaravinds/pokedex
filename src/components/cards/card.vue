<template>
  <v-card height="200">
      <div>
          <span>Pokemon Name</span>
          <span>{{pokemon.name}}</span>

      </div>
      <div>
          <span>Type</span>
          <span>{{pokemon.type}}</span>
      </div>
      <div>
          <span>Strength</span>
          <span>{{pokemon.strength}}</span>
      </div>
      <div>
          <span>Level</span>
          <span>{{pokemon.level}}</span>
      </div>
      <div>
          <span>Attacks</span>
          <span v-for="(attack, index) in pokemon.attacks" :key="index">
              {{attack}}
          </span>
      </div>
  </v-card>
</template>

<script>
export default {
    name: 'poke-card',
    data() {
        return {

        };
    },
    props: {
        pokemon: {
            type: Object,
            default() {
                return {
                    name: 'NA',
                    type: 'NA',
                    strength: 'NA',
                    level: 'NA',
                    attacks: ['NA'],
                }
            },
        },
    }
}
</script>

<style>

</style>