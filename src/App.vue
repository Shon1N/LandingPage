<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/lg.png"> -->
     <NavigationMobile />
    <div class="content" :class="{'open':showNav}">
      <div class="top-bar">
       
        <div id="navigation-icon" v-if="mobileView"
          @click="showNav = !showNav">
          <i class="fas fa-bars"></i>
        </div>
        <Navigation v-if="!mobileView" />
        <!-- <img src="./assets/lg.png" class="top-logo"> -->
      </div>
      <Content />
    </div>
  </div>
</template>
<script>
import Content from "./components/Content.vue";
import Navigation from "./components/Navigation.vue";
import NavigationMobile from "./components/NavigationMobile.vue";

export default {
  data: () => {
    return {
      mobileView: true,
      showNav: false
    };
  },
  methods: {
    handleView() {
      this.mobileView = window.innerWidth <= 990;
    }
  },
  components: {
    Navigation,
    NavigationMobile,
    Content
  },
  created() {
    this.handleView();
    window.addEventListener('resize', this.handleView);
  }
};
</script>

<style lang="scss" scoped>
@import url("https://use.fontawesome.com/releases/v5.9.0/css/all.css");

*{
box-sizing: border-box;
margin: 0;
padding: 0;
}

body{
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;  
}


#app {
  // width: calc(100% - 20px);
  height: calc(100vh - 20px);
  padding: 10px;
  color: #333;
  overflow: hidden;
}
.top-bar {
  display: flex;
  width: 100%;
}

#navigation-icon {
  padding: 10px 10px 20px;
  margin-right: 10px;
  cursor: pointer;
  i {
    font-size: 2rem;
  }
}

.content {
  position: absolute;
  top: 10px;
  padding: 19px;
  background-color: #fff;
  transition: 1s transform cubic-bezier(0,.12,.14,1);
  right: 0;
  left: 0;
}
.open {
  position: fixed !important;
  left: 259px;
  top: 9px !important;
  -moz-transition:width 2s, height 2s, background-color 2s, -moz-transform 2s;
  -webkit-transition:width 2s, height 2s, background-color 2s, -webkit-transform 2s;
  -o-transition:width 2s, height 2s, background-color 2s, -o-transform 2s;
  transition:width 2s, height 2s, background-color 2s, transform 2s;
}
</style>
