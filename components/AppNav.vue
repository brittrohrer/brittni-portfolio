<script setup>
import {ref} from "vue";

/* use variable that can be changed and create web content dynamically */
const title =ref(`Brittni Rohrer`);

</script>
<template>
    <nav class="top-nav">
        <div class="top-nav__container">
            <h1 class="top-nav__title">{{ title }}</h1>
            <ul class="top-nav__list">
                <li class="top-nav__item">
                    <NuxtLink class="top-nav__link" to="/">Home</NuxtLink>
                </li>
                <li class="top-nav__item">
                    <NuxtLink class="top-nav__link" to="/about">About</NuxtLink>
                </li>
                <li class="top-nav__item">
                    <NuxtLink class="top-nav__link" to="/projects">My Projects</NuxtLink>
                </li>
                <li class="top-nav__item">
                    <NuxtLink class="top-nav__link" to="/contact">Contact</NuxtLink>
                </li>
            </ul>
        </div>   
    </nav>
</template>
<style scoped>
</style>