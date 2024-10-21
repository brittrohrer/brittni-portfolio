<script setup>
definePageMeta({
    layout: "home"
})
const heroTitle = ref("Front End Developer");
const heroText = ref("Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sed, laboriosam.");

</script>


<template>
    <main class="page home-page">
        <div class="hero row">
            <div class="col-lg-5 hero__content">
                <h2 class="hero__title">{{ heroTitle }}</h2>
                <p class="hero__text">{{ heroText }}</p>
                <NuxtLink class="glow-on-hover" to="/contact">Contact Me!</NuxtLink>
            </div>

            <div class="col-lg-6 hero__animation">
                <i class="fa-solid fa-code"></i>
                <i class="fa-solid fa-code code-changed"></i>
            </div>
            
        </div>
    </main>
    
</template>
