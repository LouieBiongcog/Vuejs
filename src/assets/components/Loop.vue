<template>
  <ol>
    <li v-for="(item, index) in items" :key="index">
      {{ item.name }} - ${{ item.price }}
    </li>
  </ol>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { name: 'Rolex', price: 10000 },
        { name: 'Patek Phillipe', price: 5000 },
        { name: 'Jacob & Co.', price: 3000 }
      ]
    };
  }
};
</script>
