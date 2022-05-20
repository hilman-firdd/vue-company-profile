<template>
    <v-app-bar
      style="padding: 0px 160px"
      app
      color="white"
      light
      elevation="6"
      elevate-on-scroll
    >
      <v-toolbar-title>Web HilfiDev</v-toolbar-title>
      <v-spacer/>
      <v-list class="d-flex align-center">
        <v-list-item link v-for="(menu, index) in menus" :key="index" :to="menu.route">
          <v-list-item-title>{{ menu.title }}</v-list-item-title>
        </v-list-item>
        <v-btn-item>
          <v-btn text class="mx-10">
            <v-icon>mdi-magnify</v-icon>
            <v-btn outlined color="success">Get Started</v-btn>
          </v-btn>
        </v-btn-item>
      </v-list>
    </v-app-bar>
</template>

<script>
    export default {
        name: 'HeaderItem', 
        data() {
          return{
            menus: [
              {title: 'Home',       route: 'home'},
              {title: 'About Us',   route: 'about-us'},
              {title: 'Portofolio', route: 'portofolio'},
              {title: 'Project',    route: 'project'},
              {title: 'Gallery',    route: 'gallery'},
              {title: 'Contact',    route: 'Contact'},
            ]
          }
        }
    }
</script>


<style>
  .v-toolbar__title {
    font-size: 32px;
    color: #4caf50;
    font-weight: 700;
    font-family: cursive;
  }
</style>