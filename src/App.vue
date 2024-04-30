<template>
 <div>
    <HeaderSection/>
    <HeaderSectionDown/>
    <AboutSection/>
    <PortfolioSectionUp/>
    <PortfolioSectionDown/>
    <ServiceSection/>
    <TestimonialSection/>
    <BlogSection/>
    <SubscribeSection/>
    <ContactSection/>
    <MapSection/>
    <FooterSection/>
    <CustomCursor/>
    
 
 </div>
  
</template>

<script>
import HeaderSection from './components/HeaderSection.vue';
import HeaderSectionDown from './components/HeaderSectionDown.vue';
import PortfolioSectionDown from './components/PortfolioSectionDown.vue';
import ServiceSection from './components/ServiceSection.vue';
import TestimonialSection from './components/TestimonialSection.vue';
import BlogSection from './components/BlogSection.vue';
import SubscribeSection from './components/SubscribeSection.vue';
import ContactSection from './components/ContactSection.vue';
import MapSection from './components/MapSection.vue';
import FooterSection from './components/FooterSection.vue';
import AboutSection from './components/AboutSection.vue';
import PortfolioSectionUp from './components/PortfolioSectionUp.vue';
import CustomCursor from './components/CustomCursor.vue'

export default {
  name: 'App',
  components: {
   HeaderSection,
   HeaderSectionDown,
   PortfolioSectionDown,
   ServiceSection,
   TestimonialSection,
   BlogSection,
   SubscribeSection,
   ContactSection,
   MapSection,
   FooterSection,
   AboutSection,
  PortfolioSectionUp,
  CustomCursor
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  overflow-x:hidden;
}
</style>
