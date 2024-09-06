<template>
  <div>
    <h1>Total Price: ${{ totalPrice }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { name: 'Rolex', price: 10000 },
        { name: 'patek Phillipe', price: 5000 },
        { name: 'Jacob & Co.', price: 3000 }
      ]
    };
  },
  computed: {
    // A computed property to calculate the total price of all items
    totalPrice() {
      return this.items.reduce((sum, item) => sum + item.price, 0);
    }
  }
};
</script>