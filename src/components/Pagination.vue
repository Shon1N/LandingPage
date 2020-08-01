<template>
<nav aria-label="Page navigation example">
  <ul class="pagination">
    <div v-bind:key="card.id"  v-for="card in filteredCards">   
      <li class="page-item"><a class="page-link" href="#">1</a></li>
    </div>
  </ul>
</nav>
</template>

<script>
//import Cards from './Cards.vue'
import Cards from '../data/projects.vue'

console.log('Cards_pagination', Cards.data);
export default {
data(){
     return{
      cards: Cards.data,
      fCards: this.filteredCards,
      first: 'Prev',
      counter: '0',
      last: 'next',
      search: '',
    };
  },
  computed: {
 filteredCards: function(){
   return this.cards.filter((card) => {     
     return card.name.toLowerCase().match(this.search.toLowerCase());
   })   
 }
},
}

// export default {
//     name: "Pagination",
//     props: {
//         data: Cards.data,
//         visibleButtons:{
//             type: Number,
//             //required: true,
//              default: 0
//             //value: this.data,
//         },
//         visibleCards:{
//             type: Number,
//             //required: true,
//            default: 0
//         },
//         totalPages:{
//             type: Number,
//             //required: true,
//              default: 0
//             //value: this.data/8,
//         },
//         currentPage:{
//             type: Number,
//             //required: true,
//              default: 0
//         },
//     },
// };

//console.log('Cards_pagination', this.props);
</script>