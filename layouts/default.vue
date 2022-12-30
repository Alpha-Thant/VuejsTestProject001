<template>
  <v-app class="black">
    <v-app-bar
      fixed
      dense
      elevation="0"
      dark
      >      
      <v-container>
        <div class="d-flex justify-space-between">
          <span id="navTitle">
            Apple TV+
          </span>

          <span>
            <button-component buttonText="Stream now"></button-component>
          </span>
        </div>
      </v-container>
    </v-app-bar>


    <v-main class="black white--text">
      <v-container class="mt-12">
          <div class="d-flex justify-space-between topnav" id="myTopnav">
            <a style="font-size:30px;" class="icon grey--text" @click="myFunction()">&#9868;</a>
            <v-icon class="logo grey--text">mdi-apple</v-icon>
            <a id="navItem1">Store</a>
            <a id="navItem2">Mac</a>
            <a id="navItem3">iPad</a>
            <a id="navItem4">iPhone</a>
            <a id="navItem5">Watch</a>
            <a id="navItem6">AirPods</a>
            <a id="navItem7">TV & Home</a>
            <a id="navItem8">Only on Apple</a>
            <a id="navItem9">Accessories</a>
            <a id="navItem10">Support</a>
            <a ><v-icon class="bag grey--text">mdi-magnify</v-icon></a>
            <v-icon class="bag grey--text">mdi-bag-personal-outline</v-icon>
          </div>

 
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
          <p id="appleFontText1">More ways to shop: <a>Find an Apple Store</a> or <a>other retailer</a> near you. Or call 1-800-MY-APPLE.</p>
        </v-col>
      </v-row>
      <v-divider class="mb-5 mt-2"></v-divider>

      <v-row class="d-flex justify-space-between">
        <span id="appleFontText1">
          Copyright &copy; {{ new Date().getFullYear() }} Apple Inc. All rights reserved.
        </span>

        <span id="appleFontText1" >
          Privacy Policy | Terms of Use | Sales and Refunds | Legal | Site Map
        </span>

        <span id="appleFontText1">
          United States
        </span>

      </v-row>
        
    </v-container>

    </v-footer>
  </v-app>
</template>

<script>
import { onMounted } from 'vue';
import ButtonComponent from '../components/ButtonComponent.vue'
export default {
  components: { ButtonComponent },
  name: 'DefaultLayout',
  setup() {
    const myFunction = () => {
      var x = document.getElementById("myTopnav");
      var navItem1 = document.getElementById("navItem1");
      var navItem2 = document.getElementById("navItem2");
      var navItem3 = document.getElementById("navItem3");
      var navItem4 = document.getElementById("navItem4");
      var navItem5 = document.getElementById("navItem5");
      var navItem6 = document.getElementById("navItem6");
      var navItem7 = document.getElementById("navItem7");
      var navItem8 = document.getElementById("navItem8");
      var navItem9 = document.getElementById("navItem9");
      var navItem10 = document.getElementById("navItem10");



      if (x.className === "d-flex justify-space-between topnav") {
        x.className = "topnav responsive";
        navItem1.className = "navItemProp"
        navItem2.className = "navItemProp"
        navItem3.className = "navItemProp"
        navItem4.className = "navItemProp"
        navItem5.className = "navItemProp"
        navItem6.className = "navItemProp"
        navItem7.className = "navItemProp"
        navItem8.className = "navItemProp"
        navItem9.className = "navItemProp"
        navItem10.className = "navItemProp"

      } else {
        x.className = "d-flex justify-space-between topnav";
        navItem1.className = "navItemSmallProp"
        navItem2.className = "navItemSmallProp"
        navItem3.className = "navItemSmallProp"
        navItem4.className = "navItemSmallProp"
        navItem5.className = "navItemSmallProp"
        navItem6.className = "navItemSmallProp"
        navItem7.className = "navItemSmallProp"
        navItem8.className = "navItemSmallProp"
        navItem9.className = "navItemSmallProp"
        navItem10.className = "navItemSmallProp"
      }
    }

    onMounted(() => {
      navItem1.className = "navItemSmallProp"
      navItem2.className = "navItemSmallProp"
      navItem3.className = "navItemSmallProp"
      navItem4.className = "navItemSmallProp"
      navItem5.className = "navItemSmallProp"
      navItem6.className = "navItemSmallProp"
      navItem7.className = "navItemSmallProp"
      navItem8.className = "navItemSmallProp"
      navItem9.className = "navItemSmallProp"
      navItem10.className = "navItemSmallProp"
    });

    return {myFunction}
  }
}
</script>


<style scoped>

  .navItemProp {
    font-size: 17px; 
    font-weight: 400;
    font-family: 'SFProText';
    font-display: swap;
    font-stretch: 100%;
  }

  .navItemSmallProp {
    font-size: 12px; 
    font-weight: 400;
    font-family: 'SFProText';
    font-display: swap;
    font-stretch: 100%;
  }
.topnav {
  overflow: hidden;
  background-color: #000000;

}

.topnav a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  text-decoration: none;
}

.active {
  background-color: #04AA6D;
  color: white;
}

.topnav .icon {
  display: none;
}

.topnav a:hover {
  background-color: #555;
  color: white;
}

@media screen and (max-width: 820px) {
  .topnav a:not(:first-child){
    display: none;
  }
  .topnav a.icon {
    float: left;
    display: block;
  }
}

@media screen and (max-width: 820px) {
  .topnav.responsive {position: relative;}
  .topnav.responsive .icon {
    position: absolute;
    left: 0;
    top: 0;
  }

  .topnav.responsive .logo {
    float: none;
    display: block;
    text-align: center;
    margin-top: 10px;
  }

  .topnav.responsive a {
    float: none;
    display: block;
    text-align: center;
    margin-top: 10px;
  }
  .topnav.responsive .bag {
    display: none;
  }
}
</style>

