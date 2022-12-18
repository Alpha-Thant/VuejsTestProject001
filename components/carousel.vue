<template>
    <div>
        <VueSlickCarousel v-if="props.isLarge" v-bind="settings">
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

        <VueSlickCarousel v-if="!props.isLarge" v-bind="settings1">
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
      props: ['isLarge'],
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

        const settings = {
              infinite: true,
              slidesToShow: 4,
              speed: 2000,
              rows: 2,
              slidesPerRow: 1,
              autoplay: true,
              autoplaySpeed: 2000,
              centerMode: true,
            }

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

        return {
          Movies,
          settings,
          settings1,
          props,
        }
      },  
      data() {
        return {
            
        }
      }
    }
  </script> 