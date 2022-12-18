<template>
    <v-card height="200px" width="350px" class="black rounded-xl px-5 py-5">
        <v-hover v-slot="{ hover }">
            <v-card
              :class="{ 'on-hover': hover }"
            >
              <v-img
                src="https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg"
                height="200px"
                width="350px"
              >
                <v-row
                >
                <button-component 
                    class="mx-auto"
                    style="margin-top:100px;" 
                    v-if="hover" 
                    buttonText="Stream now">
                </button-component>
                </v-row>
              </v-img>
            </v-card>
          </v-hover>
        </v-card>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
export default {
  components: { ButtonComponent },
  setup() {
    const transparent = 'rgba(255, 255, 255, 0)'
   
    return {transparent}
  }
}
</script>

<style scoped>
.v-card {
  transition: opacity .4s ease-in-out;
}

.v-card .on-hover {
  opacity: 0.5;
 }
</style>
