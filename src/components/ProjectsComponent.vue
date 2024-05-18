<template>
  <div class="projects">
    <div class="categories">
      <button v-for="btn in buttonProjects" :key="btn.id" :class=btn.class @click="clickProject($event.target)">
        {{ btn.name }}
      </button>
    </div>
    <ProjectComponent v-if="visible1"/>
    <ProjectComponentBathroom v-if="visible2"/>
    <ProjectComponentKitchen v-if="visible3" />
    <div class="buttonsPages">
        <ButtonsPages v-for="button in buttons" :key="button.id" :button="button"/>
    </div>
  </div>
</template>

<script>
import ProjectComponent from './ProjectComponent.vue'
import ButtonsPages from './ButtonsPages.vue'
import ProjectComponentBathroom from './ProjectComponentBathroom.vue'
import ProjectComponentKitchen from './ProjectComponentKitchen.vue'
export default {
  name: 'ProjectsComponent',

	components: { ProjectComponent, ButtonsPages, ProjectComponentBathroom, ProjectComponentKitchen },
  data() {
    return {
      visible1: true,
      visible2: false,
      visible3: false,
      visible4: false,
      buttonProjects: [
        {
            class: "categories_btn",
            name: "Bathroom",
        },
        {
            class: "categories_btn",
            name: "Bedroom",
        },
        {
            class: "categories_btn",
            name: "Kitchen",
        },
        {
            class: "categories_btn",
            name: "Living room",
        },
      ],
      buttons: [
        {
            class: "btn-data",
            number: "01",
        },
        {
            class: "btn-data",
            number: "02",
        },
        {
            class: "btn-data",
            number: "03",
        },
        {
            class: "btn-data",
            number: "04",
        },
      ],
    };
  },

  mounted() {
    
  },

  methods: {
    clickProject(target){
      console.log(target.innerText);
      if(target.innerText == "Bathroom"){
        this.visible1 = false;
        this.visible2 = true;
        this.visible3 = false;
        this.visible4 = false;
      }
      if(target.innerText == "Bedroom"){
        this.visible1 = true;
        this.visible2 = false;
        this.visible3 = false;
        this.visible4 = false;
      }
      if(target.innerText == "Kitchen"){
        this.visible1 = false;
        this.visible2 = false;
        this.visible3 = true;
        this.visible4 = false;
      }
      if(target.innerText == "Living room"){
        this.visible1 = false;
        this.visible2 = false;
        this.visible3 = false;
        this.visible4 = true;
      }
    }
  },
};
</script>
<style>
    .projects{
        margin-top: 200px;
        margin-bottom: 200px;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
        padding: 0px;
    }
    .categories{
        border: 1px solid rgb(205, 162, 116);
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        padding: 0px;
        border-radius: 30px 30px 30px 30px;
        margin-bottom: 61px;
    }
    .categories_btn{
        width: 219px;
        border: none; outline: none; background: none;
        color: rgb(41, 47, 54);
        font-family: Jost;
        font-size: 18px;
        font-weight: 600;
        line-height: 125%;
        letter-spacing: 2%;
        text-align: center;
        padding: 26px 26px;
    }
    .categories_btn:hover{
        background-color: rgb(205, 162, 116);
        border-radius: 18px 18px 18px 18px;
    }
    .buttonsPages{
      display: flex;
      gap: 20px;
      padding-top: 50px;
    }
    .btn-data{
        border-radius: 50px 50px 50px 50px;
        padding: 14px;

        color: rgb(41, 47, 54);
        font-family: Jost;
        font-size: 16px;
        font-weight: 500;
        line-height: 150%;
        letter-spacing: 0%;
        text-align: left;
        text-transform: capitalize;

        box-sizing: border-box;
        border: 1px solid rgb(205, 162, 116);
    }
    .btn-svg{
        padding-left: 8px;
        padding-right: 5px;
        padding-top: 3px;
    }
    .btn-data:hover {
        background: rgb(244, 240, 236);
    }
</style>