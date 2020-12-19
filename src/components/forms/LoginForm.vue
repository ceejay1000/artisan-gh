<template>
  <v-card>
    <v-form>
    <v-container fluid>
      <v-row no-gutters>
        <v-col
          cols="12"
          sm="12"
        >
          <v-text-field
            v-model="username"
            label="Username"
            outlined
            dense
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="12"
        >
          <v-text-field
            v-model="email"
            label="email"
            outlined
            dense
          ></v-text-field>
        </v-col>
        <v-col
          cols="12"
          sm="12"
        >
          <v-text-field
            v-model="password"
            label="Password"
            type="password"
            outlined
            dense
          ></v-text-field>
        </v-col>
      </v-row>
      <div class="mb-4">
        <v-btn type="submit" class="mr-2" depressed white-text>Login</v-btn>
        <v-btn type="reset" elevation="0" color="red white-text">Clear</v-btn>
      </div>
      <p>Don't have an account? Register 
        <router-link 
          to="/register" 
          class="registration-link"
          >
            Here
        </router-link> 
      </p>
    </v-container>
  </v-form>
  </v-card>
</template>

<script>
export default {
  name: "LoginForm",
  data () {
    return {
      username: 'John',
      email: 'Doe',
      password: ''
    }
  }
}
</script>

<style>
a.registration-link {
  color: #200986 !important;
}
</style>
