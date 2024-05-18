<template>
  <div class="project">
    <div v-for="project in projects" :key="project.id">
      <ProjectCardDescription :project="project" />
    </div>
  </div>
</template>

<script>
import ProjectCardDescription from './ProjectCardDescription.vue'

export default {
  name: 'ProjectComponent',

	components: { ProjectCardDescription },
  data() {
    return {
      projects: [
            {
                id: 1,
                image: "progectImage1.png",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            },
            {
                id: 2,
                image: "progectImage2.png",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            },
            {
                id: 3,
                image: "progectImage3.png",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            },
            {
                id: 4,
                image: "progectImage4.png",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            },
            {
                id: 5,
                image: "progectImage5.png",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            },
            {
                id: 6,
                image: "progectImage6.png",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            },
            {
                id: 7,
                image: "progectImage7.png",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            },
            {
                id: 8,
                image: "progectImage8.png",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            }

      ],
      
    };
  },

  mounted() {
    
  },

  methods: {
    
  },
};
</script>
<style>
  .project{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
  }

</style>