<template>
  <q-page>
    <HeroSection></HeroSection>
    <AboutSection></AboutSection>
    <ServiceSection></ServiceSection>
    <TestimonialSection></TestimonialSection>
    <ContactSection id="contactSection"></ContactSection>
  </q-page>
</template>

<script setup>
import { ref, computed } from "vue";
import HeroSection from "src/components/HeroSection.vue";
import ServiceSection from "src/components/ServiceSection.vue";
import ContactSection from "src/components/ContactSection.vue"
import TestimonialSection from "src/components/TestimonialSection.vue";
import AboutSection from "src/components/AboutSection.vue";
const todoList = ref([]);
</script>
