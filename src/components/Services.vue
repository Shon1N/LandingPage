<template>
  <div id="Services">
      <div class="cards-container">
        <Cards />
      </div>
  </div>
</template>

<script>

import Cards from './Cards.vue'

export default {
name: 'Services',
components:{
  Cards
},
beforeMount: function(){

},
methods:{
  addService(obj){
    this.Cards.push(    {
      id: obj.nextId,
      name: obj.name,
      path: obj.path,
      btnText: obj.btnText,
      link: obj.link
    })
  },
    removeService(obj){
    this.Cards.push(    {
      id: obj.nextId,
      name: obj.name,
      path: obj.path,
      btnText: obj.btnText,
      link: obj.link
    })
  } ,
    updatePage(obj){
    this.Cards.push(    {
      id: obj.nextId,
      name: obj.name,
      path: obj.path,
      btnText: obj.btnText,
      link: obj.link
    })
  } ,
    updateVisibleServivesService(obj){
    this.Cards.push(    {
      id: obj.nextId,
      name: obj.name,
      path: obj.path,
      btnText: obj.btnText,
      link: obj.link
    })
  }   
}
};
</script>

<style lang="scss" scoped>


</style>