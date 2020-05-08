<template>
<div id="carousel">
<carousel :per-page="1" :mouse-drag="false" :autoplay="true" :loop="true">
  <slide
          data-index="0"
        data-name="MySlideName"
  >
   <img src="https://picsum.photos/1024/480/?image=54" width="100%">
  </slide>
  <slide
    data-index="1"
    data-name="MySlideName1"
  >
      <img src="https://picsum.photos/1024/480/?image=52" width="100%">
  </slide>
    <slide
    data-index="2"
    data-name="MySlideName2"
    >
      <img src="https://picsum.photos/1024/480/?image=58" width="100%">
  </slide>
    <slide
    data-index="3"
    data-name="MySlideName3"
    >
   <img src="https://picsum.photos/1024/480/?image=54" width="100%">
  </slide>
</carousel>
</div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';
export default {
  components: {
        Carousel,
        Slide
  }
};
</script>