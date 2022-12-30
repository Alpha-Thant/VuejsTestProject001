<template>
  <div>
    <v-row  
      justify="center" 
      align="center--text">
      <p id="appleFontTextNormal" class="mx-8">MLS Season Pass. Stream every Major League Soccer match. Coming soon.*</p>
      <a href="#">Notify me</a>
    </v-row>




    <div class="bg-wrap mt-8 white--text">
      <div class="bg-image pl-5">
        <v-container style="padding-top:250px;">
          <v-row>
            <h1 id="appleFontTitle" class="main-item">All Apple Originals.</h1>
          </v-row>
          <v-row>
            <h1 id="appleFontTitle" class="main-item">Only on Apple TV+.</h1>
          </v-row>
          <v-row class="main-item">
            <v-btn class="white black--text mt-5" style="text-transform: unset !important;" x-large rounded>Stream now</v-btn>
          </v-row>
          <v-row class="main-item" style="margin-top: 60px;">
            <h3 class="mt-3 ">Watch on the </h3>
            <img class="mx-2" width="40px" height="40px" src="@/assets/tv.png">
            <h3 class="mt-3">app</h3>
          </v-row>
        </v-container>
      </div>

    </div>



    <v-container class="white--text pl-10" style="margin-top: 0px; margin-bottom: 100px;">
      <v-row>
        <h1 id="appleFontNormalTitle" class="mx-3 fade-in">New Apple Originals every month.</h1>
      </v-row>
      <v-row class="mt-10">
        <p id="appleFontNormalTitle" class="mx-3 fade-in">Stream on the Apple TV app on Apple devices,smart TVs, consoles, or sticks</p>
      </v-row>
      <v-row class="mt-10">
        <h1 id="appleFontNormalTitle" class="mx-3 fade-in">Share Apple TV+ with your family.</h1>
      </v-row>
    </v-container>



    <v-container>
      <v-row >
        <v-col lg="3" cols="12">
          <component-one 
          class="mx-5 fade-in"
          :title="ComponentOneProp[0].title" 
          :subTitle="ComponentOneProp[0].subTitle" 
          :bodyText="ComponentOneProp[0].bodyText" 
          :buttonText="ComponentOneProp[0].buttonText"
          :showLoadMore="ComponentOneProp[0].showLoadMore"></component-one>
        </v-col>
        <v-col cols="1"></v-col>
        <v-col lg="3" cols="12">
          <component-one 
          class="mx-5 fade-in"
          :title="ComponentOneProp[1].title" 
          :subTitle="ComponentOneProp[1].subTitle" 
          :bodyText="ComponentOneProp[1].bodyText" 
          :buttonText="ComponentOneProp[1].buttonText"
          :showLoadMore="ComponentOneProp[1].showLoadMore"></component-one>
        </v-col>
        <v-col cols="1"></v-col>
        <v-col lg="3" cols="12">
          <component-one 
          class="mx-5 fade-in"
          :title="ComponentOneProp[2].title" 
          :subTitle="ComponentOneProp[2].subTitle" 
          :bodyText="ComponentOneProp[2].bodyText" 
          :buttonText="ComponentOneProp[2].buttonText"
          :showLoadMore="ComponentOneProp[2].showLoadMore"></component-one>
        </v-col>

      </v-row>
    </v-container>



    
    <v-container style="margin-top: 100px;">
      <v-carousel cycle hide-delimiter-background class="mt-10">
        <v-carousel-item
          v-for="(movie, i) in Movies"
          :key="i"
        >
          <movie-component 
            :title="movie.title"
            :des-title="movie.desTitle"
            :description="movie.description"
            :button-text="movie.buttonText">
          </movie-component>
        </v-carousel-item>
      </v-carousel>
    </v-container>

    <carousel v-if="$vuetify.breakpoint.xs" size="1" class="mt-5"></carousel>
    <carousel v-if="$vuetify.breakpoint.sm" size="2" class="mt-5"></carousel>
    <carousel v-if="$vuetify.breakpoint.md" size="3" class="mt-5"></carousel>
    <carousel v-if="$vuetify.breakpoint.lg" size="4" class="mt-5"></carousel>
    <carousel v-if="$vuetify.breakpoint.xl" size="5" class="mt-5"></carousel>

    
    <v-container fluid>
      <v-row justify="center" align="center">
        <v-btn class="white--text mb-15 mt-10" outlined large rounded style="text-transform: unset !important;">See Full lineup<v-icon small>mdi-chevron-right</v-icon></v-btn>
      </v-row>
    </v-container>





    <!-- White Section -->
    <v-container fluid class="white black--text" style="padding-top: 180px;">
      <v-row justify="center" align="center">
        <img width="80px" height="80px" src="@/assets/tv.png">
      </v-row>

      <v-row>
        <span class="mx-auto" style="text-align: center;" id="appleFontNormalTitle">Watch Apple TV+ anywhere on the Apple TV app.</span>
      </v-row>


      <v-row>
        <p class="mx-auto mt-5" style="text-align: center;" id="navItemProp"> Find the Apple TV app on your favorite Apple devices.Or watch Apple TV+ online at <a href="#">tv.apple.com.</a></p>
      </v-row>

 
    </v-container>






    <v-container fluid class="white black--text pt-15">
      <item-component></item-component>
    </v-container>







    <v-container fluid class="white black--text pt-15 pb-10">
      <v-row>
        <span class="mx-auto" style="text-align: center;" id="appleFontNormalTitle1">
          See it on your smart TV or streaming device.
        </span>
      </v-row>

      <v-row class="mt-5" justify="center" align="center">
        <a id="navItemProp">Set up your device</a>
        <v-icon small color="blue">mdi-chevron-right</v-icon>
      </v-row>

      <v-row class="mt-5" justify="center" align="center">
        <a id="navItemProp">Explore compatible devices</a>
        <v-icon small color="blue">mdi-chevron-right</v-icon>      
      </v-row>

    </v-container>






    <channel-component></channel-component>






    <v-container fluid class="white black--text pt-15">
      
      <q-and-a-component></q-and-a-component>

    </v-container>




    <v-container fluid class="white black--text pt-15">
      <v-container class="bottomComp" >
        <v-row class="my-15">
          <v-col class="pl-15" cols="12" md="5" lg="5" align="center">
            <img width="220px" v-if="$vuetify.breakpoint.smAndDown"
            src="@/assets/BottomComp/bottomComp.jpg"/>

            <img width="400px" v-if="$vuetify.breakpoint.mdAndUp" src="@/assets/BottomComp/bottomComp.jpg"/>
          </v-col>

          <v-col cols="0" md="1" lg="1"></v-col>


          <v-col cols="12" md="5" lg="5" align="center">
            <img width="100px" v-if="$vuetify.breakpoint.smAndDown" src="@/assets/BottomComp/one.png">
            <img v-else src="@/assets/BottomComp/one.png"/>

            <h1 class="mx-5" style="text-align: center;" id="appleFontNormalTitle2">
              Bundel Apple TV+ with up to five other great services.And enjoy more for less.
            </h1>
          

            <v-btn class="black white--text mt-8" large style="text-transform: unset !important;" small rounded>Try Appl One free</v-btn>

            <p class="mt-8"><a style="text-decoration: none; font-size: large;"  href="#"> Learn more <v-icon small color="blue">mdi-chevron-right</v-icon></a></p>

          </v-col>
          
      </v-row>
      </v-container>
    </v-container>






    <v-container fluid class="white black--text pt-15">
      <v-container class="bottomComp" >
        <v-row class="mt-15">
          <v-col cols="12" md="5" lg="5" align="center">
            <h1 class="mx-5" style="text-align: center;" id="appleFontNormalTitle2">
              The Apple Music Student Plan comes. with Apple TV+ for free.
            </h1> 

            <v-btn class="black white--text mt-8 mx-auto" large style="text-transform: unset !important;" small rounded>Try Appl Music free</v-btn>

          </v-col>

          <v-col cols="12" md="5" lg="5" align="center">
            <img width="200px" v-if="$vuetify.breakpoint.smAndDown"
            src="@/assets/BottomComp/bottomComp1.jpg"/>

            <img class="pl-15" width="450px" v-if="$vuetify.breakpoint.mdAndUp" 
            src="@/assets/BottomComp/bottomComp1.jpg"/>
          </v-col>
          
        </v-row>
      </v-container>
    </v-container>






    <v-container fluid class="white black--text pt-15">
      <v-container class="bottomComp" >
        <v-row>
          <v-col cols="12" lg="6" md="6" align="center">
            <div class="pb-2">
            <p class="red--text pt-15">New</p>
            <img src="@/assets/BottomComp/tv4k.png"/>
            <h1 class="mx-auto" style="text-align: center;" id="appleFontNormalTitle2">
              The Apple experience.Cinematic in every sense.
            </h1> 
      
            <v-row align="center" justify="center">
              <v-col cols="12" md="3" lg="3">
                <v-btn class="primary white--text mt-5 mr-5" large style="text-transform: unset !important;" rounded>Buy</v-btn>
              </v-col>

              <v-col cols="12" md="3" lg="3" class="mt-10">
              <p><a style="font-size: large;"> Learn more <v-icon small color="blue">mdi-chevron-right</v-icon></a></p>
              </v-col>
            </v-row>
            </div>

            <img width="250px" v-if="$vuetify.breakpoint.smAndDown"
            src="@/assets/BottomComp/bottomComp2.jpg"/>

            <img class="pl-15" width="450px" v-if="$vuetify.breakpoint.mdAndUp" 
            src="@/assets/BottomComp/bottomComp2.jpg"/>

          </v-col>

          
          <v-col cols="12" lg="6" md="6" align="center">
            <div class="bottomComp mt-5 mb-10 pb-10">
            <p class="red--text pt-13">.</p>
            <h1 >AirPlay</h1>
            <h1 class="mx-5" style="text-align: center;" id="appleFontNormalTitle2">
              Bring Apple TV+ to a screen near you.
            </h1> 

            <a style="font-size: large;"> Learn more <v-icon small color="blue">mdi-chevron-right</v-icon></a>
            </div>
            <img width="250px" v-if="$vuetify.breakpoint.smAndDown"
            src="@/assets/BottomComp/bottomComp3.jpg"/>

            <img class="mt-15" width="350px" v-if="$vuetify.breakpoint.md"
            src="@/assets/BottomComp/bottomComp3.jpg"/>

            <img class="mt-10" width="500px" v-if="$vuetify.breakpoint.lgAndUp" 
            src="@/assets/BottomComp/bottomComp3.jpg"/>
          </v-col>
      </v-row>
      </v-container>
    </v-container>




    <v-container fluid class="white pt-10" id="container">
      <v-container fluid class="bottomComp">
        <footer-component></footer-component>
      </v-container>
    </v-container>



    





  </div>

  
</template>

<script>
import ButtonComponent from '../components/ButtonComponent.vue'
import ChannelComponent from '../components/ChannelComponent.vue'
import FooterComponent from '../components/FooterComponent.vue'
import ItemComponent from '../components/ItemComponent.vue'
import MovieComponent from '../components/MovieComponent.vue'
import QAndAComponent from '../components/QAndAComponent.vue'
import SmallMovieComponent from '../components/SmallMovieComponent.vue'
import Carousel from '../components/carousel.vue'
import { onMounted, onUnmounted, reactive, ref } from 'vue'

export default {
  components: { ButtonComponent, MovieComponent, SmallMovieComponent, ItemComponent, FooterComponent, ChannelComponent, QAndAComponent, Carousel },
  name: 'IndexPage',
  setup() {

    // ComponentOne
    const ComponentOneProp = [
      {
        title: 'Buy an Apple device',
        subTitle: '3 months free.',
        bodyText: 'Apple TV+ is included for 3 months when you purchase an Apple device and redeem the offer within 90 days.1',
        buttonText: 'Check eligibility',
        showLoadMore: false,
      },
      {
        title: 'Free 7-day trial',
        subTitle: '$6.99/mo.',
        bodyText: 'A monthly subscription is just $6.99 per month after a free 7-day trial. Share Apple TV+ with your family.2',
        buttonText: 'Try it free',
        showLoadMore: false,
      },
      {
        title: 'Free 1-month trial',
        subTitle: 'Apple One',
        bodyText: 'Bundle Apple TV+ with up to five other great services for one low monthly price. And enjoy more for less.',
        buttonText: 'Try Apple One free3',
        showLoadMore: true,
      }
    ]
    


    // Movies Slide
    const Movies = [
      {
        title: "New Episode Fridays",
        desTitle: "Holiday",
        description: "Happiness is Holiday",
      },
      {
        title: "New Episode Fridays",
        desTitle: "Holiday",
        description: "Happiness is Holiday",
      },
      {
        title: "New Episode Fridays",
        desTitle: "Holiday",
        description: "Happiness is Holiday",
      },
      {
        title: "New Episode Fridays",
        desTitle: "Holiday",
        description: "Happiness is Holiday",
      },
    ]

      const fadeInElements = ref([]);
      const bg = ref([]);
      const main = ref([]);

    onMounted(() => {
      fadeInElements.value = Array.from(document.getElementsByClassName('fade-in'))
      bg.value = Array.from(document.getElementsByClassName('bg-wrap'))
      main.value = Array.from(document.getElementsByClassName('main-item'))

      document.addEventListener('scroll', handleScroll)
    });

    onUnmounted(() => {
      document.removeEventListener('scroll', handleScroll)
    });

    const handleScroll = (evt) => {

      if(main.value.length != 0) { 
        for (var j = 0; j < main.value.length; j++) {
          var mainElement = main.value[j];
          console.log(window.scrollY);
          if(window.scrollY > 80) {
            mainElement.style.opacity = "0";
          } else {
            mainElement.style.opacity = "1";
          }
        }
        
      }

      if(bg.value.length != 0) {
        var element = bg.value[0];
        var rect = element.getBoundingClientRect()
        var elemBottom = rect.bottom - 700;
        var opacity = elemBottom/window.innerHeight;
        element.style.opacity = opacity+"";

        if(window.scrollY == 0) {
          element.style.opacity = "1";
        }
      }
      

      for (var i = 0; i < fadeInElements.value.length; i++) {
        var elem = fadeInElements.value[i]
        if (isElemVisible(elem)) {
          elem.style.opacity = '1'
          elem.style.transform = 'scale(1)'
          // fadeInElements.value.splice(i, 1) // only allow it to run once
        } else {
          elem.style.opacity = '0'
          elem.style.transform = 'scale(0.8)'
        }
      }
    }


      const isElemVisible = (el) => {
        var rect = el.getBoundingClientRect()
        var elemTop = rect.top + 400 // 200 = buffer
        var elemBottom = rect.bottom
        return elemTop < window.innerHeight && elemBottom >= 0
      }


    return {
      ComponentOneProp,
      Movies,
    }
  }
}



</script>
<style>


.bg-image {
  height: 1000px; 
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
  background-image: url("@/assets/bg1.jpg");
}

.fixPostion {
  margin: 0px 200px 0px;;
}
.Heading-1 {
  font: 4.5rem sans-serif;
  font-weight: bold;
}
.Heading-2 {
  font: 2.5rem sans-serif;
  font-weight: bold;
}

.bottomComp {
  background-color:#f5f5f5;
}

#container {
  margin: 0;
  padding: 0;
}

  #navItemProp {
    font-size: 17px; 
    font-weight: 400;
    font-family: 'SFProText';
    font-display: swap;
    font-stretch: 100%;
  }


  /* fade transaction */
  .fade-in {
    opacity: 0;
    transition: 0.3s all ease-out;
    transform: scale(0.8);
    box-sizing: border-box;
    display: inline-block;
  }

  .bg-wrap {
    overflow: hidden;
    position: relative;
    opacity: 1;
    transition: 0.3s all ease-out;
  }

  .main-item {
    opacity: 1;
  }

  /* .fade-out {
    opacity: 1;
    transition: 0.3s all ease-out;
    transform: scale(1);
    box-sizing: border-box;
    display: inline-block;
  } */

</style>

