<template>
<div>
<link href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
<div class="row">
  
 <div v-bind:key="card.id"  v-for="card in cards">   
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
</template>

<script>
export default {
    name: "Cards",
data(){
  return{
    cards: [
      {
        id: 1,
        name: "Name",
        path: "https://picsum.photos/1024/480/?image=54",
        btnText: "Name",
        link: "#"
      },
      {
        id: 2,
        name: "Name",
        path: "https://picsum.photos/1024/480/?image=54",
        btnText: "Name",
        link: "#"
      },
      {
        id: 3,
        name: "Name",
        path: "https://picsum.photos/1024/480/?image=54",
        btnText: "Name",
        link: "#"
      },
      {
        id: 4,
        name: "Name",
        path: "https://picsum.photos/1024/480/?image=54",
        btnText: "Name",
        link: "#"
      },
      {
        id: 5,
        name: "Name",
        path: "https://picsum.photos/1024/480/?image=54",
        btnText: "Name",
        link: "#"
      },
      {
        id: 6,
        name: "Name",
        path: "https://picsum.photos/1024/480/?image=54",
        btnText: "Name",
        link: "#"
      }
    ]
  }
}
};
</script>

<style lang="scss" scoped>
.row {
  //display: flex;
}

.column {
 // margin: 40px; this wont work for all devices
 margin-left: auto;
 margin-right: auto;
 margin-bottom: 20%;
  //flex: 50%;
}

</style>