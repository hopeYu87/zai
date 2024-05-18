<script setup lang="ts">
const basket = useState('basket')


console.log(basket.value)
</script>

<template>
  <div>
    <h1>Card</h1>

    <table>
      <tr>
        <th>Product</th>
        <th>Price</th>
        <th>Remove</th>
      </tr>
      <tr v-for="(value, index) in basket" :key="index">
        <td>{{ value.name }}</td>
        <td>{{ value.price }}</td>
        <td>

        </td>
      </tr>
    </table>
  </div>
</template>

<style scoped>

</style>