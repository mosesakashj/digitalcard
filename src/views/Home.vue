<template>
  <div class="home">
    <Navbar />
    <div>
      <section class="container-fluid">
        <v-carousel hide-delimiters>
          <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
          ></v-carousel-item>
        </v-carousel>
      </section>
      <h1 class="display-2 pt-5"> Want To Create Your Own Digital Card</h1>
      <section class="pt-5">
        <v-parallax
    dark
    src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
    height="300"
  >
    <v-row
      align="center"
      justify="center"
    >
      <v-col
        class="text-center"
        cols="12"
      >
        <h1 class="display-1 font-weight-thin mb-4">
          Vuetify
        </h1>
        <h4 class="subheading">
          Build your own digital Card!
        </h4>
      </v-col>
    </v-row>
  </v-parallax>
      </section>
         <section>
        <v-row class="pt-5 mx-auto">
          <v-card class="col-4 mx-auto" min-height="250">
            <v-card-title>For New User</v-card-title>
            <v-btn to="/login">Click here</v-btn>
          </v-card>
          <v-card class="col-4  mx-auto" min-height="250">
            <v-card-title>For X User</v-card-title>
            <v-btn to="/login">Sign In</v-btn>
          </v-card>
        </v-row>
      </section>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/navBar.vue'

export default {
  name: 'Home',
  data(){
    return{
      items: [
          { src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg', },
          { src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg', },
          { src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',}, 
          {src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',},
        ],
    }
  },
  components: {
    Navbar
  }
}
</script>
