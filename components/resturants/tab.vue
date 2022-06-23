<template>
  <table class="w-96 table-auto border md:w-100">
    <thead class="text-left border">
      <tr>
        <th class="p-2">RANK</th>
        <th class="p-2">CHAIN</th>
      </tr>
    </thead>
    <tbody>
      <resturantsTabrow v-for="rest in grp_rests " :key="rest.id" :the_resturant="rest" :restName="rest" />
    </tbody>
  </table>
</template>

<script>

export default {
   props:["grp_rests"]

}
</script>

<style>
</style>