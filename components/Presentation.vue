<script setup>
    import { ref } from 'vue'


    import TitreNiveau2 from './TitreNiveau2.vue';
    import Courses from '@/components/Courses.vue';
    import Experiences from '@/components/Experiences.vue';
    import Skills from '@/components/Skills.vue';

    
  const presentationFilter = ref( 'courses' )
</script>

<template>
    <div id="about">
        <div class="presentation">
            <div class="presentation__text">
                <TitreNiveau2>Présentation</TitreNiveau2>
                <p>Assistante administative confirmée, à la recherche de nouveau challenge professionnel.<br> Je souhaiterais étendre mes compétences, très à l'aise avec les nombreuses activités administratives qu'exige une entreprise pour son bon fonctionnement,<br> je dispose d'un grand savoir-être et d'important savoir-faire.</p>
                <router-link class="CTA" :to="{hash:'#contact'}">Me contacter</router-link>
            </div>
        
            <img src="./assets/images/portrait.jpg" alt="Photo Amandine">
        </div>
    
        <div class="about__filter">
            <button class="about__filter__button CTA" @click="presentationFilter='courses'">Parcours</button>
            <button class="about__filter__button CTA" @click="presentationFilter='experiences'">Expériences</button>
            <button class="about__filter__button CTA" @click="presentationFilter='skills'">Compétences</button>  
        </div>
    
        <div class="about__content">
            <Courses v-if="presentationFilter === 'courses' "/>
        
            <Experiences v-if="presentationFilter === 'experiences' "/>
        
            <Skills v-if="presentationFilter === 'skills' "/>
        </div>
    </div>
</template>

<style scoped>
    .presentation {
        background-color:rgb(239, 226, 142);
        display: flex;
        padding: 10px 10%;
        gap : 20px;
        align-items: center;
    }

    .presentation__text {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 15px;
    }

    .presentation__text p {
        width: 60%;
        text-align: justify;
        text-indent: 5%;
    }

    img {
        width: 25%;
        height: 25%;
        border-radius: 50%;
        box-shadow: -4px 5px 25pxrgb(246, 229, 132);
    }

    .about__filter {
        display: flex;
        gap: 15px;
        margin: 15px 0;
        justify-content: center;
    }

    .about__content {
        margin-bottom: 15px;
        margin-bottom: 2em;
    }

    @media screen and (max-width: 480px) {
        .presentation {
            flex-direction: column-reverse;
            padding: 10px 0;
        }
        .presentation__text p {
            width: 85%;
        }
        img {
            width: 50%;
        }
    }
</style>