<template>
  <v-card 
  class="mx-auto overflow-hidden"
    height="800">
    <v-app-bar
      absolute
      color="#ff847c"
      dark
      shrink-on-scroll
      src="https://picsum.photos/1920/1080?random"
      scroll-target="#scrolling-techniques-2"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(19,84,122,.5), rgba(128,208,199,.8)"
        ></v-img>
      </template>

      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-toolbar-title>OrAsA It E1</v-toolbar-title>
    

    <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
      </v-app-bar>


    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
      
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon >
             <nuxt-link to="/">
            <v-list-item-title>Home</v-list-item-title>
             </nuxt-link>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
             <nuxt-link to="login">
            <v-list-item-title>Account</v-list-item-title>
             </nuxt-link>
          </v-list-item>

        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    <v-sheet
      id="scrolling-techniques-2"
      class="overflow-y-auto"

    >
      <v-container style="height: 150px;"></v-container>
    </v-sheet>
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