<template>
  <v-app>
    <HeaderItem />
    <v-main>
      <!-- hero section -->
      <HeroComponents/>  
      <!-- about us -->
      <AboutItem/>
      <!-- portofolio -->
      <PortofolioItem/>
      <!-- project -->
      <ProjectItem/>
      <!-- gallery -->
      <GalleryItem/>
      <!-- contact us -->
      <ContactUs/>
      <!-- footer -->
      <FooterItem/>
    </v-main>
  </v-app>
</template>

<script>

import HeaderItem from "./components/HeaderItem";
import HeroComponents from "./components/HeroComponents.vue";
import AboutItem from "./components/AboutItem.vue";
import PortofolioItem from "./components/PortofolioItem.vue";
import ProjectItem from "./components/ProjectItem.vue";
import GalleryItem from "./components/GalleryItem.vue";
import ContactUs from "./components/ContactUs.vue";
import FooterItem from "./components/FooterItem.vue";
export default {
  name: 'App',
  components: { HeaderItem, HeroComponents, AboutItem, PortofolioItem, ProjectItem, GalleryItem, ContactUs, FooterItem }
};
</script>
