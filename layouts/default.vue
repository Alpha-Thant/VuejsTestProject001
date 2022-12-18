<template>
  <v-app class="black">
    <v-app-bar
      fixed
      dense
      elevation="0"
      dark
      >      
      <v-container>
        <v-row>
          <v-col cols="2" lg="2" md="2" sm="2">
            Apple TV+
          </v-col>
          <v-col cols="2" lg="8" md="5" sm="8"></v-col>
          <v-col cols="2" lg="2" md="2" sm="2">
            <button-component buttonText="Stream now"></button-component>
          </v-col>
        </v-row>
      </v-container>
    </v-app-bar>


    <v-main class="black white--text">
      <v-container class="mt-12">
          <v-icon class="white--text">mdi-apple</v-icon>
          <span class="caption ml-15 mt-8" >Store</span>
          <span class="caption ml-10 mt-8">Mac</span>
          <span class="caption ml-10 mt-8">iPad</span>
          <span class="caption ml-10 mt-8">iPhone</span>
          <span class="caption ml-10 mt-8">Watch</span>
          <span class="caption ml-10 mt-8">AirPods</span>
          <span class="caption ml-10 mt-8">TV & Home</span>
          <span class="caption ml-10 mt-8">Only on Apple</span>
          <span class="caption ml-10 mt-8">Accessories</span>
          <span class="caption ml-10 mt-8">Support</span>
          <span class="caption ml-15"><v-icon class="white--text">mdi-magnify</v-icon></span>
          <span class="caption ml-8"><v-icon class="white--text">mdi-bag-personal-outline</v-icon></span>      
      </v-container>
      <v-divider class="mb-8 white"></v-divider>
      <Nuxt />
    </v-main>

    <v-footer
      absolute
      app
    >
    <v-container >
      <v-row>
        <v-col justify="start">
          <p>More ways to shop: <a>Find an Apple Store</a> or <a>other retailer</a> near you. Or call 1-800-MY-APPLE.</p>
        </v-col>
      </v-row>
      <v-divider class="mb-5 mt-2"></v-divider>

      <v-row>
        <v-col lg="4" cols="12" justify="start">
          Copyright &copy; {{ new Date().getFullYear() }} Apple Inc. All rights reserved.
        </v-col>

        <v-col lg="7" cols="12">
          Privacy Policy | Terms of Use | Sales and Refunds | Legal | Site Map
        </v-col>

        <v-col lg="1" cols="12">
          United States
        </v-col>

      </v-row>
        
    </v-container>

    </v-footer>
  </v-app>
</template>

<script>
import ButtonComponent from '../components/ButtonComponent.vue'
export default {
  components: { ButtonComponent },
  name: 'DefaultLayout',
}
</script>

