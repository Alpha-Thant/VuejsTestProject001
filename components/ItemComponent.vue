<template>
  <v-row justify="center" align="center"> 
    <v-col cols="4" sm="2" md="2">
      <div align="center">
          <img
              src="@/assets/AppleProducts/appletv.jpg"
              class="white--text"
              height="60px"
              width="60px"
          />
          <h4>Apple TV</h4>
      </div>
    </v-col>

    <v-col cols="4" sm="2" md="2">
      <div align="center">
          <img
              src="@/assets/AppleProducts/iphone.jpg"
              class="white--text"
              height="80px"
              width="80px"
          />
          <h4>iPhone</h4>
      </div>
    </v-col>

    <v-col cols="4" sm="2" md="2">
      <div align="center">
          <img
              src="@/assets/AppleProducts/ipad.jpg"
              class="white--text"
              height="80px"
              width="80px"
          />
          <h4>iPad</h4>
      </div>
    </v-col>

    <v-col cols="4" sm="2" md="2">
      <div align="center">
          <img
              src="@/assets/AppleProducts/mac.jpg"
              class="white--text"
              height="80px"
              width="120px"
          />
          <h4>mac</h4>
      </div>
    </v-col>

    <v-col cols="4" sm="2" md="2">
      <div align="center">
          <img
              src="@/assets/AppleProducts/airplay.jpg"
              class="white--text"
              height="90px"
              width="60px"
          />
          <h4>AirPlay</h4>
      </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
    props: ['title', 'url']
}
</script>

<style>

</style>