<template>
  <div>
    <navbar />
    <h1 class="mt-20 mb-10 mx-20 text-2xl">Restaurants page</h1>
    <!-- section contains the table -->
    <section class="mx-20 mb-20 flex flex-wrap    md:flex-nowrap md:space-y-0 lg:space-x-5 ">
      <table class="w-96 table-auto border md:w-100">
        <!-- table head -->
         <resturantsTabhead />
          <tbody>
            <!-- table rows  -->
          <ResturantsTabrow v-for="rest in first_resturants" :the_resturant="rest" :key="rest.id"     /> 
          </tbody>
      </table>
       <table class="w-96 table-auto border md:w-100 ">
        <!-- table head -->
         <resturantsTabhead class="hidden md:block"/>
          <!-- table rows  -->
          <tbody>
            <ResturantsTabrow v-for="rest in second_resturants " :the_resturant="rest" :key="rest.id" />  
          </tbody>
       </table>
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