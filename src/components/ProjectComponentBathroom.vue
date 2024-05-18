<template>
  <div class="project">
    <div v-for="project in projectsBathroom" :key="project.id">
      <ProjectCardDescriptionBathroom :project="project" />
    </div>
  </div>
</template>

<script>

import ProjectCardDescriptionBathroom from './ProjectCardDescriptionBathroom.vue';

export default {
  name: 'ProjectComponentBathroom',

	components: { 
    ProjectCardDescriptionBathroom
   },
  data() {
    return {
      projectsBathroom: [
            {
                id: 8,
                image: "progectImage8.png",
                title: "Bathroom",
                page: "Decor2 / Artchitecture2", 
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