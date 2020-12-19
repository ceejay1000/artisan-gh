<template>
  <v-app-bar color="purple" dense flat app>
    <v-btn
      depressed
      text
      normal
      color="white"
    >
      <router-link to="/" class="logo">
      <i>AGh</i>
    </router-link>
    </v-btn>

    <v-spacer></v-spacer>
    <div>
      <v-btn
      depressed
      text
      normal
      color="white"
      >
        <router-link to="/">
        Home
        <v-icon>mdi-home</v-icon>
      </router-link>
      </v-btn>
      <v-btn
      depressed
      text
      normal
      color="white"
      >
        <router-link to="/about">
        About
      </router-link>
      </v-btn>
      <v-btn
      depressed
      text
      normal
      color="white"
      >
        <router-link to="/artisans">
        Artisans
      </router-link>
      </v-btn>
      <v-btn
      outlined
      color="white"
      >
        <router-link to="/register">
          <span>Register</span>
          <v-icon>mdi-register</v-icon>
        </router-link>
      </v-btn>
    </div>
  </v-app-bar>
</template>

<script>
export default {
  name: "MainNav"
}
</script>

<style>
  a.logo,
  a.logo:link,
  a.logo:active {
    color: white !important;
    font-size: 1.8rem !important;
  }

  a {
    text-decoration: none;
    color: #fff !important;
  }
</style>
