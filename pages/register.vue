<template>
  <v-form v-model="valid">
    <center>
        <br><br>
<v-card width="1200" color="#709fb0">
      <br>
      <center><h1 v-t="'Register'" /></center>
      <v-container>
        <v-row>
          <v-col cols="12" md="6">
            <v-text-field label="name" />
          </v-col>
          <v-col cols="12" md="6">
            <v-text-field label="lastname" />
          </v-col>
          <v-col cols="12" md="6">
            <v-text-field label="username" />
          </v-col>
          <v-col cols="12" md="6">
            <v-text-field label="password" type="password" />
          </v-col>
        </v-row>
        
         <v-btn large color="purple" dark>
          Submit
          </v-btn>
      </v-container>
    </v-card>
    </center>
  </v-form>
</template>

<script>
export default {
  data: () => ({
    valid: false,
    firstname: '',
    lastname: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => v.length <= 10 || 'Name must be less than 10 characters',
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+/.test(v) || 'E-mail must be valid',
    ],
  }),
}
</script>
