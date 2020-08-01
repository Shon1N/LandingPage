<template>
  <div id="Services">
      <div class="cards-container">
        <Cards />
        <Pagination />
      </div>
  </div>
</template>

<script>

import Cards from './Cards.vue'
import Pagination from './Pagination.vue'

export default {
name: 'Projects',
components:{
  Cards,
  Pagination
},
beforeMount: function(){

},
};
</script>

<style lang="scss" scoped>


</style>