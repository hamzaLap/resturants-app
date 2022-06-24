<template>
  <tr>
    <td class="border p-2 w-32">{{ the_resturant.rank }}</td>
    <td class="border p-2"> <NuxtLink :to="`/restaurants/${the_resturant.name}`">{{ the_resturant.name }}</NuxtLink ></td>
  </tr>
</template>

<!-- :to="`/restaurants/${the_resturant.name}`" -->
<script>
export default {
  props: ["the_resturant"]
}
</script>

<style>
</style>