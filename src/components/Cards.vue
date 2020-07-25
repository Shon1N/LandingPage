<template>
<div>
<link href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
 <div class="landing-page">
   <div class="LineBreaks"></div>
 <input class="search-bar" type="text" v-model="search" placeholder="Search project">
 <div class="LineBreaks"></div>
<div class="row">
   <div v-bind:key="card.id"  v-for="card in visibleProjects"
   v-bind:visibleProjects="visibleProjects"
   v-bind:currentPage="currentPage"
   > 
   <div v-bind:key="card.id"  v-for="card in filteredCards">   
   <div class="column col-xs-6 col-sm-6 col-md-4">
  <div v-bind:id="'card-'+card.id">
    <div class="card" style="width: 18rem;">
    <img class="card-img-top" v-bind:src="card.path" v-bind:alt="card.name">
    <div class="card-body">
    <h5 class="card-title">{{card.name}}</h5>
    <p class="card-text">{{card.details}}</p>
    <a v-bind:href="card.link" class="btn btn-primary">{{card.btnText}}</a>
  </div>
    </div>
  </div>
  </div>
</div>
  </div>
  </div>
  </div>
  </div>
</template>

<script>

import projects from '../data/projects.vue'
// import func from '../../vue-temp/vue-editor-bridge';

export default {
    name: "Cards",
data(){
  console.log("Projets", projects);
  return{
    cards: projects.data,
    search: '',
    nextId: projects.data[projects.data.length - 1].id +1,
    currentPage: 0,
    pageSize: 3,
    visibleProjects: []
  };
},
computed: {
 filteredCards: function(){
   return this.cards.filter((card) => {
     return card.name.toLowerCase().match(this.search.toLowerCase());
   })
 }
}
};
</script>

<style lang="scss" scoped>
.row {
  //display: flex;
}

.search-bar{
width: 289px;
height: 44px;
}
@media screen and (min-width:572px) and (max-width:767px) {
.search-bar{
margin-left: 79px;
width: 289px;
height: 44px;
}
}

@media only screen and (min-width: 768px) {
.search-bar{
margin-left: 107px;
width: 289px;
height: 44px;
}
}

.LineBreaks{
  height: 20px;
}

.column {
 // margin: 40px; this wont work for all devices
 margin-left: auto;
 margin-right: auto;
 margin-bottom: 20%;
  //flex: 50%;
}

</style>