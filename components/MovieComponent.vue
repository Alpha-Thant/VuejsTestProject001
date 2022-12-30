<template>
    <v-card class="rounded-xl">
        <v-img
            src="https://cdn.vuetifyjs.com/images/cards/house.jpg"
            class="white--text"
            height="500px"
        >
            <v-card-subtitle id="title">{{ title }}</v-card-subtitle>
            <v-card-subtitle class="d-flex justify-space-between" style="margin-top: 320px;">
                <span id="title">{{ desTitle }}</span> .
                <span>{{ description }}</span>
                <v-btn class="white black--text" id="btn">Stream now<v-icon class="ml-1" small>mdi-play-circle</v-icon></v-btn>
            </v-card-subtitle>

        </v-img>
        </v-card>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
export default {
  components: { ButtonComponent },
    props:['title', 'desTitle', 'description']

}
</script>

<style scoped>
  #title {
    font-weight: 500;
    font-family: 'SFProDisplayTitle';
    font-stretch: 100%;
    font-size: 1em;
  }
  #btn {
    border-radius: 20px;
    text-transform: unset !important;
    margin-left: auto;
  }

</style>
