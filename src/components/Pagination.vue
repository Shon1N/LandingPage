<template>
<nav aria-label="Page navigation example">
  <ul class="pagination">
    <div v-bind:key="card.id"  v-for="card in this.Cards.data">   
      <li class="page-item"><a class="page-link" href="#">1</a></li>
    </div>
  </ul>
</nav>
</template>

<script>
//import Cards from '../data/projects.vue'
import Cards from '../data/projects.vue'

console.log('Cards_pagination', Cards);
// console.log('Cards_pagination', Cards.computed.filteredCards);
export default {
    name: "Pagination",
    props: {
        data: Cards.data,
        visibleButtons:{
            type: Number,
            //required: true,
             default: 0
            //value: this.data,
        },
        visibleCards:{
            type: Number,
            //required: true,
           default: 0
        },
        totalPages:{
            type: Number,
            //required: true,
             default: 0
            //value: this.data/8,
        },
        currentPage:{
            type: Number,
            //required: true,
             default: 0
        },
        // computed: {
        // filteredCards: function(){
        //   return this.cards.filter(() => {  
        //     //let nothing = card;
        //     console.log("this cards", this.cards);
        //     return this.cards.c;
        //     //return card.name.toLowerCase().match(this.search.toLowerCase());
        //   })   
        // }
        // },
    },


};


console.log('Cards_pagination', this.props);
</script>