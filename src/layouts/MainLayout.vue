<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="q-pa-sm">
      <q-toolbar>
    <q-img width="54px" src="../assets/brand-logo.svg"></q-img>

        <q-toolbar-title>
          Global Cloud Infotech Services LLP
        </q-toolbar-title>
        <q-space />

<!--
  notice shrink property since we are placing it
  as child of QToolbar
-->
<q-tabs v-model="tab" shrink>
  <q-tab name="tab1" label="Services" />
  <q-tab name="tab2" label="About us" />
  <q-tab name="tab3" label="Contact" @click="scrollToSection('contactSection')"/>
</q-tabs>
      </q-toolbar>
    </q-header>

   

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'



export default defineComponent({
  name: 'MainLayout',
  components: {
  },
  methods:{
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    },
  }

})
</script>
