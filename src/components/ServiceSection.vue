<template>
    <div class="service__section q-pa-md q-mb-md">
        <div class=" q-pa-md q-mb-xl"><span class="header q-pa-md"> Our Services </span></div>
        <div class="services__card-container q-pa-md">
            <q-card v-for="(service, index) in servicesList" :key="index" class="service__card">
                <q-card-section class="card__content">
                    <div class="service-icon"><i :class="service.icon"></i></div>
                    <div class="name">{{ service.name }}</div>
                    <div class="description q-pa-md">
                        {{ service.description }}
                    </div>
                </q-card-section>
            </q-card>
        </div>
    </div>
</template>

<script setup>
let servicesList = [
    {
        icon: 'bi bi-code-slash',
        name: 'Python Mastery',
        description: "Harness the versatility of Python with our expert developers. From web applications to data analysis, we craft solutions that leverage Python's capabilities to their fullest."
    },
    {
        icon: 'bi bi-cloud-arrow-up',
        name: 'AWS Cloud Excellence',
        description: "Embrace the scalability and reliability of AWS with our cloud solutions. Our certified professionals design, migrate, and manage your cloud infrastructure, ensuring optimal performance."
    },
    {
        icon: 'bi bi-boxes',
        name: 'DevOps Transformation',
        description: "Experience the agility of DevOps through our streamlined processes. We integrate development and operations, enabling rapid releases and continuous improvement."
    },
    {
        // icon:'bi bi-people',
        icon: 'bi bi-diagram-3',
        name: 'Interview Support',
        description: "Ace your technical interviews with our tailored guidance. Our seasoned professionals provide mock interviews, coaching, and insights to boost your confidence."
    }
]

</script>

<style lang="scss">
@import '../src/css/quasar.variables.scss';

.service__section {
    text-align: center;
    background-color: #f2faf5;
    padding-bottom: 3rem;

    .header {
        font-size: 2.0rem;
        font-weight: 500;
        color: $primary;
        margin: 12px 0;
        border-bottom: 2px solid $primary;

    }

    .services__card-container {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 1.5rem;

        .service__card {
            border-bottom: 3px solid $primary;
            max-width: 300px;
            -o-transition: 0.3s ease-out;
            transition: 0.3s ease-out;
            -webkit-transition: 0.3s ease-out;

            .card__content {
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
            }

            .service-icon {
                border-radius: 50%;
                font-size: 1.5rem;
                font-weight: 500;
                color: #fff;
                background-color: $primary;
                height: 64px;
                width: 64px;
                display: flex;
                justify-content: center;
                align-items: center;
                border-radius: 50px;
                background-color: rgba(0, 163, 160, .1);
                color: #00a3a0;
                margin-bottom: 1.5em;
                transition: all .3s ease-in-out;

            }

            .name {
                font-size: 1.5rem;
                color: $primary;
                font-weight: 500;
            }

            .description {}
        }

        .service__card:hover {
            background-color: $primary;
            color: #fff;

            .name {
                color: #fff;
            }

            .service-icon {
                background-color: #fff;
                color: $primary;
            }

            -ms-transform: translateY(-10px);
            transform: translateY(-10px);
            -webkit-transform: translateY(-10px);
        }

    }
}</style>