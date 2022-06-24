<template>
  <tr>
    <td class="border p-2">{{ the_resturant.rank }}</td>
    <td class="border p-2"><a :href="`/resturants/${the_resturant.name}`">{{ the_resturant.name }}</a></td>
  </tr>
</template>

<script>
export default {
  props: ["the_resturant"]
}
</script>

<style>
</style>