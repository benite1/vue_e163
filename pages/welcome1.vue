<template>
    <v-app>
        
            <br>
            <center>
               <h2><strong>WELCOME!</strong></h2>
               <p class="text--disabled">lorem ipsum dolor sit amet,<br>consectetur adipscing elit.</p>
               
               <br>
    <v-card
    class="mx-auto"
    color="#838383"
    dark
    max-width="350"
    height="400"
    >

  </v-card>
  <br>
  <nuxt-link to ="signin">
      <v-btn class="ma-2"  color="indigo" dark>Sign in</v-btn>
   
    </nuxt-link>           
            </center>
        
    </v-app>
</template>
<script>
export default {
    layout:"them1",
}
</script>