<template>
  <v-card>
        <v-img
            class="mx-auto my-12"
            :src="getImgUrl(pokemon.name)"
            contain
            >
        </v-img>
        <v-divider class="mx-4"></v-divider>
        <v-card-title>{{pokemon.name}}</v-card-title>
        <v-card-text>
            <v-row
                align="center"
                class="mx-0"
            >
                <div class="grey--text ms-4">
                    Strength
                </div>
                <v-rating
                    :value="pokemon.strength/100"
                    color="amber"
                    dense
                    half-increments
                    readonly
                    size="14"
                    title="Strength"
                ></v-rating>
                <div class="grey--text ms-4">
                    HP({{pokemon.strength}})
                </div>
            </v-row>

            <v-row
                align="center"
                class="mx-0"
            >
                <div class="grey--text ms-4">
                    Type
                </div>
                <div class="grey--text ms-4">
                    {{pokemon.type}}
                </div>
            </v-row>

             <v-row
                align="center"
                class="mx-0"
            >
                <div class="grey--text ms-4">
                    Level
                </div>
                <div class="grey--text ms-4">
                    {{pokemon.level}}
                </div>
            </v-row>

             <v-row
                align="center"
                class="mx-0"
            >
                <div class="grey--text ms-4">
                    Attacks
                </div>
             </v-row>
             <v-row
                align="center"
                class="mx-3"
            >
                <v-chip-group
                    column
                >
                    <v-chip v-for="(attack, index) in pokemon.attacks" :key="index">
                        {{attack}}
                    </v-chip>
                </v-chip-group>
            </v-row>
        </v-card-text>
  </v-card>
</template>

<script>
// const path = require('path');
export default {
    name: 'poke-card',
    data() {
        return {

        };
    },
    computed: {
        
    },
    methods: {
        getImgUrl(image) {
            return require('../../assets/pokemons/'+image+'.png?lazy')
        }
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