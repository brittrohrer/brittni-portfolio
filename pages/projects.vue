<script setup>
import {ref} from "vue";

const projects = ref([
    {
        title:  "Archery Club",
        image:  "/archery.png",
        tools:  ["HTML", 
                "CSS"
                ],
        description:"Built as a class project, this is a mockup website for a potential Archery Club. Includes web pages where future members can learn about intructors, the facility and upcoming events. ",
        code:   "https://github.com/brittrohrer/archery",
        live:   "https://brittrohrer.github.io/archery/",

    },
    {
        title:  "Adopt A Dog",
        image:  "/dogs.png",
        tools:  ["HTML", 
                "CSS", 
                "JavaScript"
                ],
        description: "Another class project to mock a pet adoption site. Includes the dog selection and checkout form.",
        code:   "https://github.com/brittrohrer/html200-adopt-a-dog",
        live:   "https://brittrohrer.github.io/html200-adopt-a-dog/",

    },
    {
        title:  "Travel Michigan",
        image:  "/mitravel.png",
        tools:  ["Bootstrap", 
                "SCSS", 
                "Vue JS/Nuxt",
                "API"
                ],
        description: "A course long project for users of the site to learn about Michigan and why to travel there. ",
        code:   "https://github.com/brittrohrer/course-project",
        live:   "https://brohrer-travel-michigan.netlify.app/",

    },
    {
        title:  "Family Recipes",
        image:  "/recipes.png",
        tools:  ["Bootstrap", 
                "SCSS", 
                "Vue JS/Nuxt"
                ],
        description:    "A personal project that takes our handwritten recipes and gathers them to a single location for everyone in our family to easlily access. ",
        code:   "https://github.com/brittrohrer/family-recipes",
        live:   "https://brohrer-family-recipes.netlify.app",

    },

])

</script>
<template>
    <main class="page">
        <h2 class="page__title">My Projects</h2>
        <section class="project">
            <ul class="project__section">
                <li
                    v-for="project in projects"
                    :key="project.title"
                    class="project">

                    <ProjectCard 
                        :title="project.title"
                        :description="project.description"
                        :image="project.image"
                        :tools="project.tools"
                        :code="project.code"
                        :live="project.live"
                    />
                </li>
            </ul>
        </section>
        <section>
            <h3 class="section-title">Code Features</h3>
        </section>
    </main>
</template>