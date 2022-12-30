<template>
    <div>
      <h3 class="white--text" id="text">{{ title }}</h3>
  
      <h1 class="white--text" id="title">{{ subTitle }}</h1>
  
      <p id="text1">{{ bodyText }} 
      <a v-if="showLoadMore" style="text-decoration: none"  href="#"> Learn more <v-icon small color="blue">mdi-chevron-right</v-icon></a></p>
      
  
      <v-btn id="btn" class="white black--text"  large rounded>{{ buttonText }}</v-btn>

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

  #title {
    font-size: 28px; 
    font-weight: 700;
    font-family: 'SFProDisplay';
    font-display: swap;
    font-stretch: 100%;
  }

  #text {
    font-size: 17px; 
    font-weight: 600;
    font-family: 'SFProText';
    font-display: swap;
    font-stretch: 100%;
  }

  #text1 {
    font-size: 17px; 
    font-weight: 400;
    font-family: 'SFProText';
    font-display: swap;
    font-stretch: 100%;
  }

  #btn {
    font-size: 14px; 
    font-weight: 700;
    font-family: 'SFProText';
    font-display: swap;
    font-stretch: 100%;
  }
  </style>