<template>
    <div>
        <h1>Каталог товаров</h1>
        <div class="product-list">
            <div v-for="product in products" :key="product.id" class="product-card">
                <img :src="product.image" alt="product.name" class="img_product" />
                <h2>{{ product.name }}</h2>
                <p>{{ product.description }}</p>
                <p>Цена: {{ product.price }} ₽</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "ProductCatalog",
    data() {
        return {
            products: [],
        };
    },
    created() {
        this.fetchProducts();
    },
    methods: {
        fetchProducts() {
            fetch('/products')
                .then(response => response.json())
                .then(data => {
                    this.products = data;
                });
        },
    },
};
</script>

<style>
.img_product {
    width: inherit;
}
.product-list {
    display: flex;
    flex-wrap: wrap;
}
.product-card {
    border: 1px solid #ccc;
    margin: 10px;
    padding: 10px;
    width: 200px;
}
</style>
