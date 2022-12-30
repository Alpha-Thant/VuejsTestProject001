<template>
    <div>
        <VueSlickCarousel v-if="props.size == 1" v-bind="settings1">
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
        </VueSlickCarousel>

        <VueSlickCarousel v-if="props.size == 2" v-bind="settings2">
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
        </VueSlickCarousel>

        <VueSlickCarousel v-if="props.size == 3" v-bind="settings3">
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
        </VueSlickCarousel>

        <VueSlickCarousel v-if="props.size == 4" v-bind="settings4">
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
        </VueSlickCarousel>

        <VueSlickCarousel v-if="props.size == 5" v-bind="settings5">
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
          <small-movie-component></small-movie-component>
        </VueSlickCarousel>

    </div>
  </template>
   
  <script>
    import VueSlickCarousel from 'vue-slick-carousel'
    import 'vue-slick-carousel/dist/vue-slick-carousel.css'
    // optional style for arrows & dots
    import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'   

    export default {
      name: 'MyComponent',
      components: { VueSlickCarousel },
      props: ['size'],
      setup(props) {
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

        

            const settings1 = {
              infinite: true,
              slidesToShow: 1,
              speed: 2000,
              rows: 2,
              slidesPerRow: 1,
              autoplay: true,
              autoplaySpeed: 2000,
              centerMode: true,
            }
            
            const settings2 = {
              infinite: true,
              slidesToShow: 2,
              speed: 2000,
              rows: 2,
              slidesPerRow: 1,
              autoplay: true,
              autoplaySpeed: 2000,
              centerMode: true,
            }

            const settings3 = {
              infinite: true,
              slidesToShow: 4,
              speed: 2000,
              rows: 2,
              slidesPerRow: 1,
              autoplay: true,
              autoplaySpeed: 2000,
              centerMode: true,
            }

            const settings4 = {
              infinite: true,
              slidesToShow: 5,
              speed: 2000,
              rows: 2,
              slidesPerRow: 1,
              autoplay: true,
              autoplaySpeed: 2000,
              centerMode: true,
            }

            const settings5 = {
              infinite: true,
              slidesToShow: 8,
              speed: 2000,
              rows: 2,
              slidesPerRow: 1,
              autoplay: true,
              autoplaySpeed: 2000,
              centerMode: true,
            }

        return {
          Movies,
          settings1,
          settings2,
          settings3,
          settings4,
          settings5,
          props,
        }
      },  
      data() {
        return {
            
        }
      }
    }
  </script> 