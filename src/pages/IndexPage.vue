<template>
  <q-page>
    <HeroSection></HeroSection>
    <ContactSection id="contactSection"></ContactSection>
  </q-page>
</template>

<script setup>
import { ref, computed } from "vue";
import HeroSection from "src/components/HeroSection.vue";
import ContactSection from "src/components/ContactSection.vue"
const todoList = ref([]);
</script>
