<template>
  <div class="mt-4">
    <v-container>
      <v-row>
        <v-col 
          xs="12" 
          sm="8" 
          md="6" 
          lg="6" 
          offset-sm="2" 
          offset-md="3">
          <div class="header header-secondary font-weight-medium">
            <h2 class="center text-h2 mb-4">Login</h2>
          </div>
          <LoginForm />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import LoginForm from "@/components/forms/LoginForm.vue";
export default {
  components: {
    LoginForm
  }
}
</script>
