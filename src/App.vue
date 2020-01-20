<template>
  <v-app>

    <v-navigation-drawer
      v-model="drawerRight"
      app
      clipped
      right
    >
      <v-list dense>
        <div class="v-subheader theme--light">
          Take a look to Auth0 + Django REST Framework
        </div>

        <!-- <v-list-item @click.stop="right = !right">
          <v-list-item-action>
            <v-icon>mdi-exit-to-app</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Open Temporary Drawer</v-list-item-title>
          </v-list-item-content>
        </v-list-item> -->

        <v-list-item @click.stop="right = !right">
          <v-list-item-action>
            <v-icon>mdi-exit-to-app</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>
              <a href="https://github.com/mcueto/djangorestframework-auth0">djangorestframework-auth0</a>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item @click.stop="right = !right">
          <v-list-item-action>
            <v-icon>mdi-exit-to-app</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>
              <a href="https://github.com/mcueto/djangorestframework-auth0_sample">djangorestframework-auth0_sample</a>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>

      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/mcueto/auth0-vue-frontend_sample"
        target="_blank"
        text
      >
        <span class="mr-2">Clone this project</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>

      <v-spacer></v-spacer>

      <v-app-bar-nav-icon @click.stop="drawerRight = !drawerRight" />

    </v-app-bar>

    <v-content>
      <!-- <HelloWorld/> -->
      <CredentialsForm/>

    </v-content>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';
import CredentialsForm from './components/CredentialsForm';

export default {
  name: 'App',

  components: {
    // HelloWorld,
    CredentialsForm,
  },

  props: {
    source: String,
  },

  data: () => ({
    drawer: null,
    drawerRight: null,
    right: false,
    left: false,
  }),

};
</script>
