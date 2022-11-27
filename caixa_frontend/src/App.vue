<template>
  <v-app>
    <AppNav/>
    <SideNav/>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import SideNav from './components/SideNav.vue'
import AppNav from './components/AppNav.vue'

export default {
  name: 'App',

  data: () => ({
    //
  }),
  components:{
    SideNav:SideNav,
    AppNav:AppNav
  }
}
</script>
