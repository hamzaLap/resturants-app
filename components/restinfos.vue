<template>
<main>
  <!-- title -->
    <h1 class="text-center   text-6xl  my-5 md:mb-16"  > {{the_restaurant.name}}</h1>
    <!-- description -->
   <p  class="px-5 font-medium mb-10 text-justify text-xl font-normal md:w-3/4  md:mb-15 md:px-10 md:leading-relaxed lg:mb-20 lg:text-2xl  lg:leading-loose md:mx-auto" >{{  this.the_restaurant.content}}</p>
   <!-- images and more infos -->
   <div class="flex max-w-3xl mb-16 mx-10 flex-col flex-col md:flex-row md:mx-auto md:space-x-6 ">
     <div class="flex justify-center items-center my-7">
       <img class="rounded max-w-sm max-h-64 " :src="the_restaurant.imageUrl" :alt="the_restaurant.name">
   </div>
   <section class="w-3/4 mx-16  text-xl font-medium my-5 flex flex-col space-y-5 items-center justify-center">
      <div  class="w-full flex justify-between" ><h1 class="w-full">rank is </h1> <span  class="mx-auto" >{{the_restaurant.rank}}</span></div>
     <div  class="w-full flex justify-between"  > <h1>number of stores</h1> <span> {{the_restaurant.numberOfStores}}</span></div>
     <div  class="w-full flex justify-between"  > <h1>revenue is</h1> <span>{{the_restaurant.revenue}}</span> </div>
    </section>
   </div>

</main>
</template>

<script>
export default {
  head(){
    return{
      title:this.the_restaurant.name
    }
  },
props:["the_restaurant"]
}
</script>
