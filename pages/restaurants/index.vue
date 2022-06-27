<template>
  <div class="bg-slate-50">
    <navbar />
    <div>

      <font-awesome-icon :icon="['fas', 'user']" />
    </div>
    <h1 class="mt-20  ml-10 text-4xl  my-5 md:mb-16 md:text-center lg:text-5xl">Restaurants page</h1>
    <!-- section contains the table -->
    <section class="ml-10 max-w-2xl mb-20 flex flex-wrap md:flex-nowrap md:space-y-0 lg:space-x-5 lg:mx-auto">
      <table class="w-96 table-auto border md:w-100">
        <!-- table head -->
         <resturantsTabhead />           
            <!-- table rows  -->
            <tbody>
              <ResturantsTabrow v-for="rest in first_resturants " :the_resturant="rest" :key="rest.id" /> 
            </tbody>
          
      </table>
       <table class="w-96 table-auto border md:w-100 ">
        <!-- table head -->
         <resturantsTabhead class="hidden md:table-row"/>
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