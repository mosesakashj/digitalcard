<template>
  <div>
     <v-container grid-list-xl text-xs-center>
       <v-layout row wrap>
         <v-row class="mx-auto container-fluid">
           <v-card dark color="dark" elevation-24 style="padding: 20px; my-auto mx-auto">
             <v-card-text>
               <h4 class="display-2 font-weight-bold pb-3">Login</h4>
               <v-divider class="px-4"></v-divider>
               <v-form>
                 <v-text-field clearable v-model="username" label="Username" prepend-icon="mdi-face" type="text" color="white" counter="10"></v-text-field>
                 <v-text-field clearable v-model="password" label="Password" prepend-icon="mdi-lock" type="password" color="white"></v-text-field>
              </v-form>
              <br>
               <v-btn color="grey darken-2" large>Enter</v-btn>
             </v-card-text>
           </v-card>
         </v-row>
       </v-layout>
     </v-container>
</div>
</template>

<script>
export default {
data() {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    prependClicked() {
      console.log('prepend clicked');
    },
    appendClicked() {
      console.log('append clicked', this.username);
    }
  }
}
</script>

<style>

</style>