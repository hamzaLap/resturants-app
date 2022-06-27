<template>
<div >
  <div  class="h-4 text-xl bg-red-100"
  >

      <font-awesome-icon :icon="['fas', 'user']" />
    </div>
  <NuxtLink to="/restaurants">
    <button class="w-20  bg-green-200 m-5 rounded hover:bg-green-300" >back</button>
  </NuxtLink>
  <!-- render the specified restaurant -->
  <main v-if="the_restaurant">
        <restinfos :the_restaurant="the_restaurant"/>
  </main>
  <!-- not find page -->
  <div v-else >
    <!-- componenet for restaurants error -->
    <resterror/>
  </div>
    <restFooter/>
</div>
</template>

<script>

import resturantsObj from "@/data.json"

export default {
  created(){
             
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