<template>
   <div>
    <h1>Product List</h1>

    <ul>
        <li v-for="(product , index) in filteredProducts" :key="index">
             <span v-if="product.onSale" class="badge">On Sale</span>
            {{ product.name }} - ${{ product.price }}
        </li>
    </ul>

    <div>
        <label for="filterPrice"> Filter by price:</label>
        <input v-model.number="filterPrice" id="filterPrice" type = "number" placeholder="enter max price">
    </div>
   </div>
</template>

<script>
export default{
    data(){
        return{
            product:[
                {name: 'laptop', price: 10000, onSale: true},
                {name: 'Mouse', price: 10000, onSale: true},
                {name: 'Keyboard', price: 10000, onSale: true},
                {name: 'Speaker', price: 10000, onSale: true},
            ],
            filterPrice: 10000
        };
    },
    computed:{
        filterProducts(){
            return this.product.filter(product => product.price <= this.filterPrice);
        }
    }

};


</script>

<style>
    .badge{
        background-color: black;
        color: green;
        padding: 2px;
        margin-right: 5px;
        border-radius: 3px;
    }
</style>
