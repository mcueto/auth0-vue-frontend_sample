<template>
  <v-form v-model="valid">
    <v-container>

      <v-text-field
        v-model="auth0Domain"
        label="AUTH0_DOMAIN"
        required
      ></v-text-field>

      <v-text-field
        v-model="auth0ClientID"
        label="AUTH0_CLIENT_ID"
        required
      ></v-text-field>

      <v-text-field
        v-model="auth0ClientSecret"
        label="AUTH0_CLIENT_SECRET"
        required
      ></v-text-field>

      <v-text-field
        v-model="auth0Audience"
        label="AUTH0_AUDIENCE"
        required
      ></v-text-field>

    </v-container>
  </v-form>

</template>

<script>
export default {
  name: 'CredentialsForm',

  data: () => ({
    valid: false,
    auth0Domain: '',
    auth0ClientID: '',
    auth0ClientSecret: '',
    auth0Audience: '',
    // nameRules: [
    //   v => !!v || 'Name is required',
    //   v => v.length <= 10 || 'Name must be less than 10 characters',
    // ],
    // emailRules: [
    //   v => !!v || 'E-mail is required',
    //   v => /.+@.+/.test(v) || 'E-mail must be valid',
    // ],
  }),
};
</script>
