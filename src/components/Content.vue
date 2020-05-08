<template>
  <div id="content">
     <img alt="Vue logo" src="" class="logo" >
    <div class="info-container">
        <Carousel />
        <Services />
        <About />
    </div>
  </div>
</template>
   
<script>
import Carousel from "./Carousel.vue";
import About from "./About.vue";
import Services from "./Services.vue";
export default {
  components: {
      Carousel,
      About,
    Services,
  },    
};
</script>

<style lang="scss" scoped>
#content{

}
.info-container {
  position: relative;
  width: 100%;
  margin-bottom: 40px;
//   background-image: url("../assets/takeabreak.jpg");
  background-size: cover;
  background-position: top;
//   border-radius: 20px;
  overflow: hidden;
}

// .logo{
//     width: 80%;
//     margin-top: -103px;
//     margin-left: 62px;
// }

.logo{
    width: 80%;
    margin-top: -103px;
    margin-left: 62px;
}

@media only screen and (min-width: 1030px) {
.logo {
    margin-top: -37px;
    margin-left: 10px;
    margin-bottom: 30px;
    width: 55%;
}
}


</style>