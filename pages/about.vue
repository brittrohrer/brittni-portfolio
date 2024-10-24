<script setup>

const aboutHeader =ref(`Hello, I'm Brittni`);

const aboutText = ref([`I grew up in Northern Michigan. My love for travel, 
experiencing different cultures, and design guided me to my degrees in Archaeology and Geographic Information Systems (GIS).`,

`During my college years I studied abroad in Belize, where I specialized in Maya Archaeology. After my return to the US, 
I participated on a few more archeological projects within Michigan. 
Though I'm not currently working on any digs, I am still traveling whenever possible. Including, traveling solo to Costa Rica to learn to surf.`,

`My eye for design came into play in GIS. Although, GIS is more than just designing and creating maps. 
It is effectively displaying geographical/spatial data for the audience to use and understand. This is also a useful skill to contribute 
to my future in web development. `]);

const aboutImg = ref([
    {
        src: "https://images.pexels.com/photos/4588057/pexels-photo-4588057.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
        alt: "pic of me",
    }
    ]);

const skills = ref([
    {
        name: "Git",
        logo: "fa-brands fa-square-git skill__logo"
    },
    {
        name: "HTML",
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
        name: "SCSS",
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
        logo: "nuxt-logo skill__logo"
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
            <div class="col-md-7 ">
                <p class="about-me__text" v-for="text in aboutText" :key="text">{{ text }}</p>
            </div>
            <div class="col-md-5">
                <img class="about-me__img img-fluid" v-for="img in aboutImg" :key="img.src" :src="img.src" :alt="img.alt">
            </div>
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