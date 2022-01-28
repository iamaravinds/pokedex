<template>
  <v-container>
    <v-row>
      <v-col
        v-for="n in 12"
        :key="n"
        cols="4"
      >
      <Card/>
        <!-- <v-card height="200"></v-card> -->
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  import Card from '@/components/cards/card';
  export default {
    name: 'Home',
    components: {
      Card,
    },
    data: () => ({
      
    }),
  }
</script>
