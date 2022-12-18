<template>
    <v-card class="rounded-xl">
        <v-img
            src="https://cdn.vuetifyjs.com/images/cards/house.jpg"
            class="white--text"
            height="500px"
        >
            <v-card-subtitle>{{ title }}</v-card-subtitle>
            <v-card-subtitle style="margin-top: 350px;">
                {{ desTitle }} .
                {{ description }}
                <button-component style="margin-left:70%;" buttonText="Stream now"></button-component>
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
