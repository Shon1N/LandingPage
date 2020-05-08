<template>
  <div id="Services">
      <div class="cards-container">
        <Cards v-bind="cards" />
      </div>
  </div>
</template>

<script>

import Cards from './Cards.vue'

export default {
name: 'Services',
components:{
  Cards
}
};
</script>

<style lang="scss" scoped>


</style>