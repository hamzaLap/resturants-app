<template>
<main>

    <section>
       <h1> {{the_restaurant.name}}</h1>
       <h1>rank is {{the_restaurant.rank}}</h1>
       <h1>number of stores {{the_restaurant.numberOfStores}}</h1>
       <h1>revenue is {{the_restaurant.revenue}}</h1>
     </section>
      <div>
        <img :src="the_restaurant.imageUrl" :alt="the_restaurant.name">
    
        <p>{{  this.the_restaurant.content}}</p>
    </div>
</main>
</template>

<script>
export default {
props:["the_restaurant"]
}
</script>
