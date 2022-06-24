<template>
<div>
  <NuxtLink to="/restaurants">
    <button class="w-20  bg-green-200 m-5 rounded hover:bg-green-300" >back</button>
  </NuxtLink>
 <section>
   <h1> {{rest_name}}</h1>
   <h1>rank is {{the_restaurant.rank}}</h1>
   <h1>number of stores {{the_restaurant.numberOfStores}}</h1>
   <h1>revenue is {{the_restaurant.revenue}}</h1>
 </section>
  <div>
    <img :src="the_restaurant.imageUrl" :alt="the_restaurant.name">

    <p>{{  this.the_restaurant.content}}</p>

</div>
</div>
</template>

<script>
import resturantsObj from "@/data.json"

export default {
  mounted(){
    this.the_restaurant=resturantsObj.find(rest => rest.name==this.rest_name)
  },
data(){
  return{
    rest_name:this.$route.params.names,
    the_restaurant: {}
  }
}
}
</script>
var name =
<style>

</style>