<template>
  <v-app>
      <v-system-bar
          color="#e2979c"
          :height="height"
          :lights-out="lightsOut"
          :window="window"
        >
          
          <v-spacer></v-spacer>
          <v-icon>mdi-wifi-strength-4</v-icon>
          <v-icon>mdi-signal-cellular-outline</v-icon>
          <v-icon>mdi-battery</v-icon>
          <span>12:37</span>
        </v-system-bar>

         <v-card>
    <v-toolbar class="primary">
        <v-btn icon>
          <n-link to="welcome1">
        <v-icon class="white--text">mdi-arrow-left</v-icon>
        </n-link>
      </v-btn>
      

      <v-toolbar-title>Welcome</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <template v-slot:extension>
        <v-tabs
          v-model="tabs"
          fixed-tabs
        >
          <v-tabs-slider></v-tabs-slider>
          <v-tab
            href="#mobile-tabs-10-1"
            class="white--text"
          >
            <nuxt-link to="signup"><p class="white--text">SIGN UP</p></nuxt-link>
            
          </v-tab>

          <v-tab
            href="#mobile-tabs-10-2"
            class="white--text"
          >
            <nuxt-link to="signin"><p class="white--text">SIGN IN</p></nuxt-link>
          </v-tab>

        </v-tabs>
      </template>
    </v-toolbar>

    <v-tabs-items v-model="tabs">
      <v-tab-item
        v-for="i in 3"
        :key="i"
        :value="'mobile-tabs-6-' + i"
      >
        <v-card flat>
          <v-card-text v-text="text"></v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>


        <v-content>
            <nuxt/>
        </v-content>
  </v-app>
    
       
</template>

