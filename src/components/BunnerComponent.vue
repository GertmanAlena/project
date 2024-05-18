<template>
  <div class="bunner">
    <img src="../assets/projectBunner.png" alt="bunner__image">
    <div class="bunner__text">
        <h1 class="bunner__title">Our Project</h1>
        <div class="bunner__menubar">
          <a class="active new" href="#">Home</a>
          <a class="active" href="#">Progect</a>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BunnerComponent',

  data() {
    return {
      
    };
  },

  mounted() {
    
  },

  methods: {
    
  },
};
</script>
<style>
    a{
      text-decoration: none;
    }
    .bunner{
      display: flex;
      justify-content: center;
      position: relative;
    }
    .bunner__title{
      margin-bottom: 2px;
    }
    .bunner__menubar{
      display: flex;
      gap: 10px;
    }
    .bunner__text{
      border-radius: 37px 37px 0px 0px;
      background: rgb(255, 255, 255);
      position: absolute;
      width: 169px;
      height: 72px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 40px 150px 40px 150px;
      top: 204px;
    }
    .active{
      color: rgb(77, 80, 83);
      font-family: Jost;
      font-size: 22px;
      font-weight: 400;
      line-height: 150%;
      letter-spacing: 1%;
      text-align: left;
    }
    .new::after {
      content: "/";
      padding-left: 10px;
    }
</style>
