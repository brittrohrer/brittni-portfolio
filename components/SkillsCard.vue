<script setup>

import {defineProps, ref} from "vue";


/* Image Prop
   - Create Prop with simple type validator
   - Declare what type of variables and what type of data we are recieving from the parent
*/
const prop = defineProps({
        name: String,
        logo: String,
        

});
</script>
<template>
    <div>
        <div>
            <i :class="prop.logo"></i>
            <p class="skill__name">{{ prop.name }}</p>
        </div>
    </div>
</template>