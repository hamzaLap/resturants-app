<template>
  <table class="w-96 table-auto border md:w-100">
    <thead class="text-left border">
      <tr>
        <th class="p-2" >RANK</th>
        <th class="p-2" >CHAIN</th>
      </tr>
    </thead>
    <tbody>
      <resturantsTabrow v-for="(rest , index) in Rests" :key="rest" :rank="index"   :restName="rest"  />
    </tbody>
  </table>
</template>

<script>
export default {
  data(){
    return{

       Rests:["hamza","jamal","farid","ahmed","salim","tariq","kamal","brahim"]
    }

  }

}
</script>

<style>

</style>