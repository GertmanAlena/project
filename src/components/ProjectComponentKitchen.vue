<template>
  <div class="project">
    <div v-for="project in projectsKitchen" :key="project.id">
      <ProjectCardDescriptionKitchen :project="project" />
    </div>
  </div>
</template>

<script>
import ProjectCardDescriptionKitchen from './ProjectCardDescriptionKitchen.vue';


export default {
  name: 'ProjectComponentKitchen',

	components: { ProjectCardDescriptionKitchen },
  data() {
    return {
      projectsKitchen: [
            {
                id: 1,
                image: "kitchen1.jpg",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            },
            {
                id: 2,
                image: "kitchen2.jpg",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            },
            {
                id: 3,
                image: "kitchen3.jpg",
                title: "Minimal Bedroom",
                page: "Decor / Artchitecture", 
                alt: "Minimal image",
                class: "projectClass",
                classImage: "image-class"
            },          
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