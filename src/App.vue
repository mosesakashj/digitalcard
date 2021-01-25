<template>
  <v-app light>
    <div>
      <!-- <nav>
        <v-toolbar id="navbar" >
            <v-app-bar-nav-icon @click="side= !side" v-if="!$vuetify.breakpoint.smAndUp"></v-app-bar-nav-icon>
            <v-toolbar-title>
              <span class="font-weight-black pr-3">Digital Card Builder</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn text class="text-capitalize primary--text text--darken-2" v-for="(item, i) in navItems" :key="i" :href="item.link"><v-icon left v-text="item.icon"></v-icon><h4>{{ item.text}}</h4></v-btn>
        </v-toolbar> -->
      <!-- </nav> -->
      <v-main>
        <v-container fluid>
            <router-view /> 
        </v-container>
      </v-main>
    </div>
  </v-app>
</template>
<script>
export default {
  data(){
    return{
      side:false,
      transitionName: 'scale-transition',
      navItems: [
        { text: 'Home', icon: '', link: '' },
        { text: 'About Us', icon: '', link: '' },
        { text: 'Contact Us', icon: '', link: '' }
      ],
    }
  },methods:{
    logout() {
      this.$store.commit('RemoveAuth',{status:false,username:null,admin:false})
      this.$router.push({ name: "Home" })
    }
  },
  mounted() {
    // this.$store.commit('getActiveUser')
    // this.$root.$on('AlertUser',(title, state)=>{ this.snackbar.title=title, this.snackbar.state=state})
    // this.$route.name !== "Dashboard" && this.$store.state.authenticated ?  this.$router.replace({ name: "Dashboard" }) : false
    // this.$route.name !== "Home" && !this.$store.state.authenticated ?  this.$router.push({ name: "Home" }) : false
  }
}
</script>

<style>
#navbar a{
  color: black;
  padding-inline-end: 3%;
  text-align: center;
  padding: 10px 20px;
  text-decoration: none;
}
#navbar a:hover{
   background-color:grey;
    color: white;
}
</style>
