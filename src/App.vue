<template>
	<v-app>
		<v-app-bar app color="primary" dark>
			<v-toolbar-title>Vuetify Dashboard</v-toolbar-title>
			<v-spacer></v-spacer>
			<v-btn text rounded>Home</v-btn>
			<v-btn text rounded>Login</v-btn>
		</v-app-bar>
    
    <NavigationDrawer/>
    
    
      
    <!-- login -->
    <v-container></v-container>
    <v-container fluid>
    <v-card width="400" class="mx-auto mt-5">
      <v-card-title>
        <h1 class="display-1">Σύνδεση</h1>
      </v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field
            label="Όνομα Χρήστη"
            prepend-icon="mdi-account-circle"
            variant="underlined"
            />
            <v-text-field
            :type="showPassword ? 'text':'password'"
            label="Κωδικός Πρόσβασης"
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'mdi-eye': 'mdi-eye-off'"
            @click:append="showPassword=
            !showPassword"
            variant="underlined"
            />
        </v-form>
      </v-card-text>
      <v-divider></v-divider>
      <v-card-actions>
        <v-btn 
        block
        color="secondary"
        variant="elevated">ΣΥΝΔΕΣΗ</v-btn>
      </v-card-actions>
    </v-card>
    </v-container>  

  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import NavigationDrawer from './components/NavigationDrawer.vue'
export default {
  name: 'App',

  components: {
    HelloWorld,
    NavigationDrawer
  },

  data: () => ({
    showPassword:false,
    drawer:true,
    links: ['Home', 'Login'],
  }),
}
</script>
