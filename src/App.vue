<template>
  <v-app>
    <v-card width="400" class="mx-auto mt-5">
      <v-card-title>
        <h1 class="display-1">Σύνδεση</h1>
      </v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field
            label="Όνομα Χρήστη"
            prepend-icon="mdi-account-circle"
            />
            <v-text-field
            :type="showPassword ? 'text':'password'"
            label="Κωδικός Πρόσβασης"
            prepend-icon="mdi-lock"
            append-icon="mdi-eye-off"
            @click:append="showPassword=
            !showPassword"
            />
        </v-form>
      </v-card-text>
      <v-divider></v-divider>
      <v-card-actions>
        <v-btn color="info">ΣΥΝΔΕΣΗ</v-btn>
      </v-card-actions>
    </v-card>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    showPassword:false
  }),
}
</script>
