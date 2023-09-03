<template>
    <div class="testimonial-section q-pa-md">
        <!-- <q-carousel animated v-model="activeSlide" navigation infinite :autoplay="autoplay" arrows transition-prev="slide-right"
            transition-next="slide-left" @mouseenter="autoplay = false" @mouseleave="autoplay = true">
            <q-carousel-slide :name="index" class="column no-wrap flex-center" > -->
        <div class=" q-pa-md q-mb-lg"><span class="header q-pa-md"> Discover What Our Clients Say About Us </span></div>
        
        <div class="testimonial__cards-container q-pa-md">
            <q-card v-for="(testimonial, index) in testimonials" :key="index" class="testimonial-card q-pa-md">
                <q-card-section>
                    <div class="comment-icon"><i class="bi bi-quote"></i></div>
                    <div class="comment">
                        {{ testimonial.comment }}
                    </div>
                </q-card-section>
                <q-card-section>
                    <div class="name">
                        {{ testimonial.name }}
                    </div>
                    <div>{{ testimonial.designation }}</div>
                </q-card-section>
            </q-card>
        </div>
        <!-- </q-carousel-slide>
        </q-carousel> -->
    </div>
</template>
  
<script setup>
import { ref } from 'vue';

let activeSlide = ref(0);
let cardHeight = '300px'// Adjust the card height as needed
let testimonials = [
    {
        name: '- Emily Watson',
        designation: ' CEO, DataWave Analytics',
        comment: '“Global Cloud Infotech Services revolutionized our approach to technology. Their Python expertise transformed our data analysis capabilities, giving us a competitive edge in the market.”'
    },
    {
        name: '- Michael Chen',
        designation: ' CTO, CloudMinds Inc.',
        comment: '“The AWS solutions provided by Global Cloud Infotech Services enhanced our scalability and reduced operational complexities. Partnering with them was a game-changer for our business.”'
    },
    {
        name: '- Sarah Rodriguez',
        designation: 'Director of Engineering, NexGen Software',
        comment: '“DevOps seemed like a distant dream until we collaborated with Global Cloud Infotech Services. Their strategies streamlined our development pipeline, increasing efficiency and collaboration.”'
    }
    // Add more testimonials as needed
]

</script>
  
<style scoped lang="scss">
/* Import Quasar variables */
@import '../src/css/quasar.variables.scss';

.testimonial-section {
    text-align: center;
    // background-color: #f2faf5;
    padding-bottom: 3.5rem;
    .header {
        font-size: 2.0rem;
        font-weight: 500;
        color: $primary;
        margin: 12px 0;
        border-bottom: 2px solid $primary;

    }

    .testimonial__cards-container {
        display: flex;
        justify-content: center;
        gap: 3.0rem;
        flex-wrap: wrap;

        .testimonial-card {
            max-width: 300px;
            text-align: left;

            .comment-icon{
                font-size: 2.5rem;
                color: $primary;
            }
            .comment{
                line-height:2;
            }

            .name {
                font-weight: 500;
                font-size: 1.0rem;
            }

        }
    }

}
</style>
  