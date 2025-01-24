<script setup>
    import TitreNiveau2 from './TitreNiveau2.vue';

    const competences = ['HTML', 'CSS', 'JavaScript', 'Vue.JS']

    const languages = [
        {
            name: "Français",
            level: "Langue maternelle"
        },
           ]

    const hobbies = [
        {
            name: 'Voyages',
        },
        {
            name: 'Randonnée'
        },
        {
            name: 'Lire'
        }
    ]
</script>

<template>
    <p><h3>Experiences professionnelles</h3></p>
        <h4><b>Assistante de Production - Excent</b></h4>
                            <p>Mai 2019 à aujourd'hui </p>
                        <ul>
                            <li>Gestion demande client</li>
                            <li>Création - suivi d'indicateur de performance</li>
                            <li>Suivi de planning dans le logiciel de Gestion d'Affaire</li>
                        </ul>
                        <h4><b><br>Employée Administrative </b></h4>
                            <p>2016 - 2019 </p>
                        <ul>
                            <li>Accueil Physique et téléphonique</li>
                            <li>Gestion Devis / Factures</li>
                            <li>Planification et organisation de la production</li>
                        </ul>
                        <h4><b><br>Assistante Commerciale d'Appels d'Offre</b></h4>
                            <p>Juin-Octobre 2016</p>
                        <ul>
                            <li>Gestion des dossier d'Appels d'Offre</li>
                            <li>Gestion suivi courrier</li>
                        </ul>
                </div>

    
        <div class="right__column">
            <div class="outils">
                <div class="outils__title">
                    <span class="material-symbols-outlined">menu_book</span>
                    <TitreNiveau2>Outils maîtrisés</TitreNiveau2>
                </div>
                <div class="outils__content">
                    <ul>
                        <li v-for="i in tools" class="tool">
                            {{ i.name }} : {{ i.liste }}
                        </li>
                    </ul>
                </div>
            </div>

            <div class="hobbies">
                <div class="hobbies__title">
                    <span class="material-symbols-outlined">fitness_center</span>
                    <TitreNiveau2>Centres d'interêt</TitreNiveau2>
                </div>
                <div class="hobbies__content">
                    <ul>
                        <li v-for="i in hobbies" class="hobby">
                            {{ i.name }}
                            <ul>
                                <li class="sousListe" v-for="e in i.liste">{{ e }}</li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .competences {
        width: 60%;
        display: flex;
        flex-direction: row;
        align-items: center;
        margin: auto;
        align-content: center;
        justify-content: center;
        gap: 15px;
        flex-wrap: wrap;
    }

    .skills, .languages, .outils, .hobbies {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: auto;
        margin-top: 15px;
    }

    .skills__title, .languages__title, .outils__title, .hobbies__title {
        display: flex;
        align-items: center;
        text-align: center;
    }

    .material-symbols-outlined {
        font-size: 2.5em;
    }

    .skills__content, .languages__content {
        margin-top: 15px;
        display: flex;
        gap: 15px;
        flex-wrap: wrap;
        justify-content: center;
    }

    .competence, .language {
        list-style-type: none;
        color: white;
        background-color:rgb(253, 225, 115);
        padding: 5px 1em;
        border-radius: 1em;
        box-shadow: -4px 4px 10pxrgb(248, 166, 43);
    }

    .hobby {
        margin-top: 10px;
        text-align: start;
    }

    .sousListe {
        list-style-type: circle;
    }

    .hobbies__content, .outils__content {
        align-self: flex-start;
        margin: 15px 0;
    }

    @media screen and (max-width: 480px) {
        .competences {
            width: 85%;
        }
    }
</style>