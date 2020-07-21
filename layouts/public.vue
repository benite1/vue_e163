<template>
<v-app id=colorbg>
  
   <!-- ใส่ข้อความ -->
  <v-main>
    <v-container fluid>
     <v-content>
       <nuxt/>
     </v-content>
    </v-container>
  </v-main>
  
  <v-footer>
      <v-bottom-navigation
    v-model="bottomnav"
    dark
    shift
     absolute
    
  >
  
    <v-btn>
     
      <nuxt-link to="login"><span>ACCOUNT</span></nuxt-link>
      <v-icon>mdi mdi-account-circle</v-icon>
    </v-btn>

    <v-btn>
       <nuxt-link to="/"><span>HOME</span></nuxt-link>
      <v-icon>mdi mdi-home-variant</v-icon>
    </v-btn>

    <v-btn>
       <nuxt-link to="/actiity/menu"><span>MENU</span></nuxt-link>
    <v-icon>mdi-apps</v-icon>
    </v-btn>

    <v-btn>
       <nuxt-link to="home"><span>IMAGE</span></nuxt-link>
      <v-icon>mdi-image</v-icon>
    </v-btn>
   
  </v-bottom-navigation>
  </v-footer>
  </v-app>
  
</template>

<script>
  export default {
    data () {
      return {
        bottomNav: 3,
      }
    },

    computed: {
      color () {
        switch (this.bottomNav) {
          case 0: return 'blue-grey'
          case 1: return 'teal'
          case 2: return 'brown'
          case 3: return 'indigo'
        }
      },
    },
  }
</script>
 <style>
 #colorbg {
 background: linear-gradient(to right, #0099ff 0%, #ff9999 100%);
 } </style>
