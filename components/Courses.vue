<script setup>
    import TitreNiveau2 from './TitreNiveau2.vue';

    const parcours = {
        annee1: {
            ecole: 'PIGIER',
            date: '2011-2013',
            title: 'Bac Pro Administratif',
            comment: 'alternance'
        },
        annee2: {
            ecole: 'PIGIER',
            date: '2014',
            title: 'Bac+2 Gestionnaire de Petite et Moyenne Structure',
            comment: "alternance"
        },
        annee3: {
            ecole: 'EFC',
            date: '2015',
            title: 'Formation Gestionnaire de Paie',
            comment: 'à distance'
        },
       
    }
</script>

<template>
    <div class="courses">
        <div class="courses__title">
            <span class="material-symbols-outlined">school</span><br>
            <TitreNiveau2>Mon parcours</TitreNiveau2>
        </div>
    
        <div class="parcours">
            <div class="ecole" v-for="annee in parcours">
                <h3 class="ecole__title">{{ annee.ecole }}</h3>
                <h4 class="ecole__info">{{ annee.title }} <span class="separation">|</span> {{ annee.date }}</h4>
                <p class="ecole__comment">{{ annee.comment }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .courses {
        width: 60%;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: auto;
    }

    .courses__title {
        text-align: center;
    }

    .material-symbols-outlined {
        font-size: 4em;
    }

    .ecole__title {
        font-size: 1.25em;
    }

    .ecole__info {
        font-size: 1.05em;
    }

    .separation {
        font-style: italic;
        color:rgb(15, 2, 67);
    }

    .ecole__comment {
        text-indent: 2em;
        text-align: justify;
    }

    .parcours {
        margin-top: 15px;
        display: flex;
        flex-direction: column-reverse;
        gap: 25px;
    }

    .ecole {
        padding: 15px;
        background-color: #EFFAFD;
        border-radius: 25px;
        box-shadow: -4px 5px 10pxrgb(3, 79, 56);
    }

    @media screen and (max-width: 480px) {
        .courses {
            width: 85%;
        }
    }
</style>