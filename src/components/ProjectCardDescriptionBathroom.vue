<template>
  <div :class="project.class">
    <img :class="project.classImage" :src="imgUrl" alt="image" v-on:click="visible=!visible" >
    <img class="star"  src="..//assets/projectImages/Star.png" alt="star" v-show="visible">
    <div class="projectClass_btn">
      <div>
        <h3>{{ project.title }}</h3>
        <p>{{ project.page }}</p>
      </div>
      <button class="options__button">
        <svg width="10.000000" height="21.000000" viewBox="0 0 10   21" fill="none" xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink">
          <defs />
          <path id="Vector" d="M1 19L9 10L1 1" stroke="#292F36" stroke-opacity="1.000000" stroke-width="2.000000"
            stroke-linejoin="round" stroke-linecap="round" />
        </svg>
      </button>
    </div>
  </div>
</template>

<script>

export default {
  name: 'ProjectCardDescriptionBathroom',
  props: {
    project: {
      type: Object,
      required: false,
    }
  },
  data() {
    return {
      visible: false,
    };
  },
  computed: {
    imgUrl() {
      return require(`@/assets/projectImages/${this.project.image}`)
    },
    imgAlt() {
      return `Изображение проекта ${this.project.alt}`
    }
  },
  mounted() {

  },

  methods: {

  },

};
</script>
<style scoped>
.star{
  left: 536px;
  position: absolute;
}
.options__button {
  width: 70px;
  height: 70px;
  background-color: rgb(244, 240, 236);
  border-radius: 50%;
  border: none;
  vertical-align: top;
}

.projectClass_btn {
  display: flex;
  justify-content: space-between;
  padding-top: 17px;
  align-items: center;
}

.projectClass {
  position: relative;
}

</style>