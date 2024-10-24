<script setup>

import {defineProps, ref} from "vue";


/* Image Prop
   - Create Prop with simple type validator
   - Declare what type of variables and what type of data we are recieving from the parent
*/
const prop = defineProps({
        title: String,
        tools: Array,
        image: String,
        description: String,
        code: String,
        live: String

});
</script>
<template>
        <div class="row project__card">
            <div class="project__img-container col-md-6 col-lg-5">
                <img class="project__img" :src="prop.image">
            </div>
            <div class="col-md-6 col-lg-7 project__text">
                <h3 class="project__title">{{ prop.title }}</h3>
                <p class="project__description">{{ prop.description }}</p>
                <ul class="project__tools-list">
                    <li class="project__tools-item" v-for="tool in tools" :key="tool[0]">{{ tool }}</li>
                </ul>
                <a class="project__link project__link--code" :href="prop.code" target="blank">Code >></a>
                <a class="project__link project__link--live" :href="prop.live" target="blank">Website >></a>
            </div>
        </div>
</template>