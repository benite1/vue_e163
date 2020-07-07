<template>
  <center>
    <div>
      <br>
      <h1 v-t="'สมุดบันทึกกิจกรรม'" />
    </div>
    <div class="my-2">
      <v-btn color="success" fab x-large dark>
        <v-icon>mdi-account-circle</v-icon>
      </v-btn>
      <nuxt-link to="/activity/menu/">
        <v-btn class="my-2" fab x-large dark color="teal">
          <v-icon dark>
            mdi-format-list-bulleted-square
          </v-icon>
        </v-btn>
      </nuxt-link>
    </div>
  </center>
</template>
