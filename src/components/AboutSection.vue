<template>
    <div class="about__section q-pa-md q-mb-md">
        <div class="about__content-block">
            <div class="q-mb-lg">
            <span class="header q-pb-md">About Us</span>
        </div>
        <div class="content">
            At TechNex Solutions, we believe that technology holds the key to unlocking infinite possibilities. Our journey began with a vision to bridge the gap between businesses and technology, and today, we stand as a leading IT company committed to delivering transformative solutions. With a team of dedicated experts and a customer-centric approach, we take pride in driving digital evolution for our clients.
        </div>
        <q-btn @click="scrollToSection('contactSection')" class="q-mt-lg " style="background: #194a70;color:#fff" label="Contact Us" />

        </div>
      
        <div class="about__img"><q-img src="../assets/about-us.png"></q-img></div>
    </div>
</template>
<script setup>
   function scrollToSection(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    }
</script>
<style lang="scss">
/* Import Quasar variables */
@import '../src/css/quasar.variables.scss';

.about__section {
    display: flex;
    justify-content: space-around;
    .about__content-block{
        width: 60%;
        max-width: 650px;
        .header {
        font-size: 2.0rem;
        font-weight: 500;
        color: $primary;
        margin: 24px 0;
        border-bottom: 2px solid $primary;
    }
    .content{
        font-size: 1rem;
        line-height: 2;
    }
    }
    .about__img{
        width: 40%;
    }
  
}
</style>