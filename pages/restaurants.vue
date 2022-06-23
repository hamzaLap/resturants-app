<template>

  <div>
    <navbar />
    <h1 class="mt-20 mb-10 mx-20 text-2xl">Restaurants page</h1>
    <section class="mx-20 mb-20 flex flex-wrap space-y-5 md:flex-nowrap md:space-y-0 lg:space-x-5 ">
      <resturantsTab :grp_rests="first_resturants" />
      <resturantsTab  :grp_rests="second_resturants"/>
    </section>


  </div>

</template>

<script>
import resturants from "@/data.json"

export default {
  mounted(){
      //  this.Resturants=JSON.parse(resturants),
       this.Resturants=[...resturants]
       this.first_resturants=this.Resturants.splice(0,25),
       this.second_resturants=this.Resturants.splice(0,25)
       console.log(this.second_resturants);
    },
  data(){
   return{
         Resturants:[],
         first_resturants:  [] ,
         second_resturants:[]    
        }
      }
}
</script>

<style>

</style>