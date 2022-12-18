<template>
    <div>
      <h3 class="white--text">{{ title }}</h3>
  
      <h1 class="white--text">{{ subTitle }}</h1>
  
      <p>{{ bodyText }} 
      <a v-if="showLoadMore" style="text-decoration: none"  href="#"> Learn more <v-icon small color="blue">mdi-chevron-right</v-icon></a></p>
      
  
      <v-btn class="white black--text" style="text-transform: unset !important;" large rounded>{{ buttonText }}</v-btn>

    </div>
  </template>
  
  <script>
  import ButtonComponent from './ButtonComponent.vue'
  export default {
  components: { ButtonComponent },
      props: ['title', 'subTitle', 'bodyText', 'buttonText', 'showLoadMore'],
  }
  </script>
  
  <style scoped>
  p {
    color: cadetblue;
  }
  </style>