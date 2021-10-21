<template>
  <div class="wrapper">
      <img src="../assets/Web_Developer.jpg" alt="Pc workspace" id="landing_img">
      <div class="central_text" @click="$emit('active', active)">
          <h1>Hi! I'm Denis Paul</h1>
          <p>and I'm a junior web-developer!</p>
          <p class="small">click here to go to the website</p>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Landing',
    data() {
        return {
            active: 1
        }
    }
}
</script>

<style lang="scss" scoped>
    #landing_img {
        width: 100%;
        height: 100vh;
    }
    .wrapper {
        height: 100vh;
    }
    .central_text {
        display: inline-block;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        padding: 25px 50px;
        padding-bottom: 0;
        border-radius: 10px;
        text-align: center;
        color: white;
        background-color: rgba(255, 101, 0, .6);

        &:hover {
            cursor: pointer;
            background-color: rgb(255, 101, 0);
        }
        .small {
            font-size: 10px;
            padding-top: 20px;
        }

        p {
            font-size: 22px;
        }
    }

</style>