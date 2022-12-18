<template>
  <div>
    <v-row :class="{'body-2': $vuetify.breakpoint. smAndDown, 
      'caption': $vuetify.breakpoint. mdAndUp}"  
      justify="center" 
      align="center--text">
      <p class="ml-5">MLS Season Pass. Stream every Major League Soccer match. Coming soon.*</p>
      <a href="#">Notify me</a>
    </v-row>



    <div class="bg-image mt-8 pl-5 white--text">
      <v-container  style="padding-top:250px;">
      <v-row >
        <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">All Apple Originals.</h1>
      </v-row>
      <v-row >
        <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">Only on Apple TV+.</h1>
      </v-row>
      <v-row >
        <v-btn class="white black--text mt-10" style="text-transform: unset !important;" x-large rounded>Stream now</v-btn>
      </v-row>
      <v-row style="margin-top: 80px;">
        <h3 class="mt-3">Watch on the </h3>
          <img class="mx-2" width="40px" height="40px" src="@/assets/tv.png">
        <h3 class="mt-3">app</h3>
      </v-row>
      </v-container>
    </div>



    <v-container class="white--text pl-10" style="margin-top: 300px; margin-bottom: 100px;">
      <v-row>
        <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">New Apple Originals every month.</h1>
      </v-row>
      <v-row class="mt-10">
        <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">Stream on the Apple TV app on Apple</h1>
      </v-row>
      <v-row>
        <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">devices,smart TVs, consoles, or sticks</h1>
      </v-row>
      <v-row class="mt-10">
        <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">Share Apple TV+ with your family.</h1>
      </v-row>
    </v-container>



    <v-container>
      <v-row>
        <v-col lg="3" cols="12">
          <component-one 
          :title="ComponentOneProp[0].title" 
          :subTitle="ComponentOneProp[0].subTitle" 
          :bodyText="ComponentOneProp[0].bodyText" 
          :buttonText="ComponentOneProp[0].buttonText"
          :showLoadMore="ComponentOneProp[0].showLoadMore"></component-one>
        </v-col>
        <v-col cols="1"></v-col>
        <v-col lg="3" cols="12">
          <component-one 
          :title="ComponentOneProp[1].title" 
          :subTitle="ComponentOneProp[1].subTitle" 
          :bodyText="ComponentOneProp[1].bodyText" 
          :buttonText="ComponentOneProp[1].buttonText"
          :showLoadMore="ComponentOneProp[1].showLoadMore"></component-one>
        </v-col>
        <v-col cols="1"></v-col>
        <v-col lg="3" cols="12">
          <component-one 
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

    <carousel v-if="$vuetify.breakpoint.smAndDown" :isLarge="false" class="mt-5"></carousel>
    <carousel v-if="$vuetify.breakpoint.mdAndUp" :is-large="true" class="mt-5"></carousel>

    
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

      <v-row justify="center" align="center">
        <h1 :class="{'subtitle-2': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">Watch Apple TV+ anywhere</h1>
      </v-row>

      <v-row justify="center" align="center">
        <h1 :class="{'subtitle-2': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">on the Apple TV app.</h1>
      </v-row>

      <v-row class="mt-10" justify="center" align="center">
        <div :class="{'body-2': $vuetify.breakpoint. smAndDown, 
      'caption': $vuetify.breakpoint. mdAndUp}"> Find the Apple TV app on your favorite Apple devices.</div>
      </v-row>

      <v-row justify="center" align="center">
        <div :class="{'body-2': $vuetify.breakpoint. smAndDown, 
      'caption': $vuetify.breakpoint. mdAndUp}">Or watch Apple TV+ online at <a href="#">tv.apple.com.</a></div>
      </v-row>
 
    </v-container>






    <v-container fluid class="white black--text pt-15">
      <item-component></item-component>
    </v-container>







    <v-container fluid class="white black--text pt-15 pb-10">
      <v-row justify="center" align="center">
        <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">See it on your smart TV</h1>
      </v-row>

      <v-row justify="center" align="center">
        <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">or streaming device.</h1>
      </v-row>


      <v-row class="mt-5" justify="center" align="center">
        <a>Set up your device</a>
        <v-icon small color="blue">mdi-chevron-right</v-icon>
      </v-row>

      <v-row class="mt-5" justify="center" align="center">
        <a>Explore compatible devices</a>
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

          <img width="500px" v-if="$vuetify.breakpoint.mdAndUp" src="@/assets/BottomComp/bottomComp.jpg"/>
          </v-col>
          <v-col cols="1"></v-col>
          <v-col cols="12" md="5" lg="5" align="center">
            <img src="@/assets/BottomComp/one.png"/>

            <h1 class="mt-5" :class="{'heading': $vuetify.breakpoint. smAndDown, 
            'display-3': $vuetify.breakpoint. mdAndUp}">Bundel Apple TV+ with</h1>
            <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
            'display-3': $vuetify.breakpoint. mdAndUp}">up to five other great services.</h1>
            <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
            'display-3': $vuetify.breakpoint. mdAndUp}">And enjoy more for less.</h1>

            <v-btn class="black white--text mt-8" large style="text-transform: unset !important;" small rounded>Try Appl One free</v-btn>

            <p class="mt-8"><a style="text-decoration: none; font-size: large;"  href="#"> Learn more <v-icon small color="blue">mdi-chevron-right</v-icon></a></p>

          </v-col>
          
      </v-row>
      </v-container>
    </v-container>






    <v-container fluid class="white black--text pt-15">
      <v-container class="bottomComp" >
        <v-row class="mt-15">
          <v-col cols="12" md="5" lg="5" class="ml-5" align="start">
            <h1 class="mt-5" :class="{'heading': $vuetify.breakpoint. smAndDown, 
            'display-3': $vuetify.breakpoint. mdAndUp}">The Apple Music</h1>
            <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
            'display-3': $vuetify.breakpoint. mdAndUp}">Student Plan comes.</h1>
            <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
            'display-3': $vuetify.breakpoint. mdAndUp}">with Apple TV+ for free.</h1>

            <v-btn class="black white--text mt-8" large style="text-transform: unset !important;" small rounded>Try Appl Music free</v-btn>

          </v-col>

          <v-col cols="12" md="5" lg="5" align="center">
            <img width="220px" v-if="$vuetify.breakpoint.smAndDown"
            src="@/assets/BottomComp/bottomComp1.jpg"/>

            <img class="pl-15" width="500px" v-if="$vuetify.breakpoint.mdAndUp" 
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
            <h1 class="mt-3" :class="{'heading': $vuetify.breakpoint. smAndDown, 
            'display-3': $vuetify.breakpoint. mdAndUp}">The Apple experience.</h1>
            <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
            'display-3': $vuetify.breakpoint. mdAndUp}">Cinematic in every sense.</h1>
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

            <img class="pl-15" width="570px" v-if="$vuetify.breakpoint.mdAndUp" 
            src="@/assets/BottomComp/bottomComp2.jpg"/>

          </v-col>

          
          <v-col cols="12" lg="6" md="6" align="center">
            <div class="bottomComp pb-5">
            <p class="red--text pt-13">.</p>
            <h1 >AirPlay</h1>
            <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
            'display-3': $vuetify.breakpoint. mdAndUp}">Bring Apple TV+ to</h1>
            <h1 class="pb-5" :class="{'heading': $vuetify.breakpoint. smAndDown, 
            'display-3': $vuetify.breakpoint. mdAndUp}">a screen near you.</h1>
            <a style="font-size: large;"> Learn more <v-icon small color="blue">mdi-chevron-right</v-icon></a>
            </div>
            <img width="250px" v-if="$vuetify.breakpoint.smAndDown"
            src="@/assets/BottomComp/bottomComp3.jpg"/>

            <img class="pl-15" width="570px" v-if="$vuetify.breakpoint.mdAndUp" 
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


    return {
      ComponentOneProp,
      Movies,
    }
  }
}
</script>
<style>
.bg-image {
  height: 700px; 
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
</style>

