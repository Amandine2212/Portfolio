<script setup>
    import { computed } from 'vue'

    const copyright = computed(() =>{
        const currentYear = new Date().getFullYear()
        return `© Copyright ${currentYear} | Hugo Melin`
    });
</script>

<template>
    <footer class="footer">
        <div class="footer__content">
            <div class="footer__adress">
                <h3>Mes contacts</h3>
                <address>
                    <a href="mailto:amandine.larrosa@outlook.fr">amandine.larrosa@outlook.fr</a>
                    <a href="tel:0601010101">06.01.01.01.01</a>
                    <p>72000 Le Mans</p>
                </address>
            </div>
            <div class="footer__borderRight"></div>
            <div class="footer__social">
                <h3>Me contacter</h3>
                <a class="footer__social__icon" href="https://github.com/Amandine2212" target="_blank" rel="noopener noreferrer">
                    <img src="@/assets/images/logogithub.png" alt="Logo GitHub">
                </a>
                <a class="footer__social__icon" href="https://www.linkedin.com/feed/" target="_blank" rel="noopener noreferrer">
                    <img src="@/assets/images/logolinkedin.png" alt="Logo LinkedIn">
                </a>
            </div>
        </div>
        <div class="footer__copyright">
            <p>Dernières modifications le<time datetime="2025-01-22">22 janvier 2025</time></p>
            <p class="copyright">{{ copyright }}</p>
        </div>
    </footer>
</template>

<style scoped>
    .footer__content {
        display: flex;
        justify-content: space-evenly;
    }

    footer * {
        background-color:rgb(251, 191, 106);
        color: white;
        padding: 10px;
    }
    
    .footer__borderRight {
        border-right: 1px solid #EFFAFD;
    }

    address {
        display: flex;
        flex-direction: column;
    }

    .footer__copyright {
        text-align: center;
    }

    time {
        font-style: italic;
    }

    .copyright {
        font-style: italic;
        font-size: 0.8em;
    }

    .footer__social__icon:hover {
        opacity: 50%;
    }
</style>