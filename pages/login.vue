<template>
  <v-app>
    <center>
      <br><br>
      <v-card width="1000" height="300" color="#726a95">
        <v-card-title>
          <h1>Login</h1>
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field label="Username" prepend-icon="mdi-account-circle" />
            <v-text-field
              prepend-icon="mdi-lock"
              :append-icon="show3 ? 'mdi-eye' : 'mdi-eye-off'"
              :rules="[rules.required, rules.min]"
              :type="show3 ? 'text' : 'password'"
              name="input-10-2"
              label="Password"
              hint="At least 8 characters"
              value=""
              class="input-group--focused"
              @click:append="show3 = !show3"
            />
          </v-form>
        </v-card-text>
        <v-card-actions>
          <nuxt-link to="register">
            <v-btn large color="success" dark>
              Regiter
            </v-btn>
          </nuxt-link>
          <v-spacer />
          <v-btn large color="purple" dark>
            Login
          </v-btn>
        </v-card-actions>
      </v-card>
    </center>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      show3: false,
      password: 'Password',
      rules: {
        required: value => !!value || 'Required.',
        min: v => v.length >= 8 || 'Min 8 characters',
        emailMatch: () => ('The email and password you entered don\'t match'),
      },
    }
  },
}
</script>
