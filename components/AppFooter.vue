<script setup>
import {ref} from "vue";
const contactEmail = ref("brittnirohrer@gmail.com");

const connections = ref([
    {
        icon:`fa-brands fa-square-github connect__icon`,
        link:`https://github.com/brittrohrer?tab=repositories`
    },
    {
        icon:`fa-brands fa-linkedin connect__icon`,
        link:`https://www.linkedin.com/in/brittni-rohrer-3183212b6/`
    }
])    
const copyright = ref(`Brittni Rohrer | Oct. 2024`);
</script>

<template>
    <footer class="footer">
        <div>
            <p class="email-address">Email: {{ contactEmail }}</p>
        </div>
        <div class="connect">
            <div class="connect__links-container">
                <a class="connect__link" v-for="icon in connections" :key="icon" :href="icon.link">
                    <i :class="icon.icon"></i>
                </a>
            </div>
        </div>
        <div class="copyright">
            <p class="copyright__text"> {{ copyright }}</p>
        </div>
    </footer>
</template>
