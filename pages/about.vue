<script setup>

const aboutHeader =ref(`Hello, I'm Brittni`);

const aboutText = ref(`I grew up in Northern Michigan. My love for travel, 
experiencing different cultures, and design guided me to my degrees in Archaeology and Geographic Information Systems (GIS).

During my college years I studied abroad in Belize, where I specialized in Maya Archaeology. After my return to the US, 
I participated on a few more archeological projects within Michigan. 
Though I'm not currently working on any digs, I am still traveling whenever possible. Including, traveling solo to Costa Rica to learn to surf.

My eye for design came into play in GIS. Although, GIS is more than just designing and creating maps. 
It is effectively displaying geographical/spatial data for the audience to use and understand. This is also a useful skill to contribute 
to my future in web development. `);

const aboutImg = ref([
    {
        src: "https://images.unsplash.com/photo-1606589329778-e87fbc5b7e33?w=900&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NjF8fHByb2ZpbGUlMjBwaWN0dXJlfGVufDB8fDB8fHwy",
        alt: "pic of me",
    }
    ]);

const skills = ref([
    {
        name: "git",
        logo: "fa-brands fa-square-git skill__logo"
    },
    {
        name: "html",
        logo: "fa-brands fa-html5 skill__logo"
    },
    {
        name: "JavaScript",
        logo: "fa-brands fa-js skill__logo"
    },
    {
        name: "CSS",
        logo: "fa-brands fa-css3-alt skill__logo"
    },
    {
        name: "Sass",
        logo: "fa-brands fa-sass skill__logo"
    },
    {
        name: "Bootstrap",
        logo: "fa-brands fa-bootstrap skill__logo"
    },
    {
        name: "Vue JS",
        logo: "fa-brands fa-vuejs skill__logo"
    },
    {
        name: "Terminal",
        logo: "fa-solid fa-terminal skill__logo"
    },
    {
        name: "Nuxt",
        logo: "skill__logo"
    },

])

const educationSection = ref([
    {
        school: `North Central Michigan College`,
        degree: `Associate of Arts`,
    },
    {
        school: `Central Michigan University`,
        degree: `Bachelor of Science: Concentration in Geographic Information Systems, Concentration in Anthropology: Archaeology`
    },
    {
        school: `University of Washington`,
        degree: `Front-end Web Development Certificate`,
    },
    
])
</script>
<template>
    <main class="page">
        <h2 class="page__title">About Me</h2>
        <section class="row about-me">
            <h3 class="about-me__header">{{ aboutHeader }}</h3>
            <p class="col-sm-7 about-me__text">{{ aboutText }}</p>
            <img class="col-sm-5 about-me__img" v-for="img in aboutImg" :key="img.src" :src="img.src" :alt="img.alt">
        </section>
        <section>
            <h3 class="section-title">Skills</h3>
            <ul class="skill">
                <li class=skill__item v-for="skill in skills" :key="skill.name">
                    <SkillsCard 
                    :name="skill.name"
                    :logo="skill.logo" />
                </li>
            </ul>
        </section>
        <section>
            <h3 class="section-title">Education</h3>
            <ul class="education">
                <li class="education__list-item" v-for="education in educationSection" :key="education.school">
                    <h4 class="education__school">{{ education.school }}</h4>
                    <p class="education__degree">{{ education.degree }}</p>
                </li>
            </ul>
        </section>
        <section>
            <h3 class="section-title">Resume</h3>
            <a href="/public/Rohrer-Resume.pdf" class="resume-link" type="pdf" target="blank">View Resume</a>
        </section>
    </main>
</template>