<script>
import ProductItem from './ProductItem.vue'
export default {

    name: 'ProductList',
    props: ['products'],
    components: {ProductItem},
    data(){
        return{
            
        }
    },
    methods: {
      
    }
}

</script>

<template>
  <div class="product-list">
        <h2>Product List</h2>
        <div class="list-container">
          <ProductItem v-for="product in products" :key="product.id" :product="product" />
        </div>
        
  </div>
</template>
<style scoped>
.product-list{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    background-color: #f0f0f0;
    border: 1px solid #ccc;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0,0,0,0
    5);
    }
    .list-container{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        padding: 20px;
        }
</style>