<template>
    <v-app>
        <center>
            <br><br>
    <v-avatar color="grey" size="120">
    </v-avatar>
        <br><br>
         <v-col cols="12" sm="4">
          <v-text-field
            label="username"
          
            solo
          ></v-text-field>

          <v-text-field
            label="password"
            solo
          ></v-text-field>
        </v-col>

        </center>

         <v-checkbox
         class="ma-5"
      v-model="checkbox"
      :rules="[v => !!v || 'You must agree to continue!']"
      label="Remember me"
      required
      margin="50"
    ></v-checkbox>
           <!-- <nuxt-link to="forgot"><p class="white--text">Forgot password</p></nuxt-link> -->


           <v-btn class="ma-10" tile color="indigo" dark>Sign in</v-btn>
    </v-app>
</template>
<script>
export default {
    layout:"them2",
}
</script>