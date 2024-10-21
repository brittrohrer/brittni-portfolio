<script setup>
import {ref} from "vue";

const projects = ref([
    {
        title:  "Archery Club",
        image:  "https://images.unsplash.com/photo-1457305237443-44c3d5a30b89?q=80&w=2948&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
        tools:  ["HTML", 
                "CSS"
                ],
        description:    "description Lorem ipsum odor amet, consectetuer adipiscing elit. Eros eu laoreet lectus litora auctor sit ac nisi. Turpis ut convallis rutrum nec natoque amet. Elit amet at molestie congue conubia malesuada facilisis. Velit et felis erat senectus ultrices porttitor diam eleifend.",
        code:   "https://github.com/brittrohrer/archery",
        live:   "https://brittrohrer.github.io/archery/",

    },
    {
        title:  "Adopt A Dog",
        image:  "https://images.unsplash.com/photo-1457305237443-44c3d5a30b89?q=80&w=2948&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
        tools:  ["HTML", 
                "CSS", 
                "JavaScript"
                ],
        description:    "description Lorem ipsum odor amet, consectetuer adipiscing elit. Eros eu laoreet lectus litora auctor sit ac nisi. Turpis ut convallis rutrum nec natoque amet. Elit amet at molestie congue conubia malesuada facilisis. Velit et felis erat senectus ultrices porttitor diam eleifend.",
        code:   "https://github.com/brittrohrer/html200-adopt-a-dog",
        live:   "https://brittrohrer.github.io/html200-adopt-a-dog/",

    },
    {
        title:  "Travel Michigan",
        image:  "https://images.unsplash.com/photo-1457305237443-44c3d5a30b89?q=80&w=2948&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
        tools:  ["Bootstrap", 
                "Scss", 
                "Vue"
                ],
        description:    "description Lorem ipsum odor amet, consectetuer adipiscing elit. Eros eu laoreet lectus litora auctor sit ac nisi. Turpis ut convallis rutrum nec natoque amet. Elit amet at molestie congue conubia malesuada facilisis. Velit et felis erat senectus ultrices porttitor diam eleifend.",
        code:   "https://github.com/brittrohrer/course-project",
        live:   "https://brohrer-travel-michigan.netlify.app/",

    },

])

</script>
<template>
    <main class="page">
        <h2 class="page__title">My Projects</h2>
        <section>
            <h3 class="section-title">Full Websites</h3>
            <ul>
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