<template>

  <v-card 
  class="mx-auto overflow-hidden"
    height="800"
    >
    
    
       <v-content>
            <nuxt/>
        </v-content>
  </v-card>
</template>
<script>
  export default {
    data: () => ({
      drawer: false,
    }),
  }
</script>

