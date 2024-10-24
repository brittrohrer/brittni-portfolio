<script setup>
definePageMeta({
    layout: "home"
})
const heroTitle = ref("Front End Developer");
const heroText = ref("Builder of accessible and responsive websites");

</script>


<template>
    <main class="page home-page">
        <div class="hero row">
            <div class="col-xl-6 hero__content">
                <h2 class="hero__title">{{ heroTitle }}</h2>
                <p class="hero__text">{{ heroText }}</p>
                <NuxtLink class="glow-on-hover" to="/contact">Contact Me!</NuxtLink>
            </div>

            <div class="col-xl-5 hero__animation">
                <i class="fa-solid fa-code"></i>
            </div>
            
        </div>
    </main>
    
</template>
