<template>
    <div>
        <h2>{{ product.name }}</h2>
        <p>{{ product.description }}</p>
        <p>Цена: {{ product.price }}</p>
    </div>
</template>

<script>
export default {
    name: "Product",
    props: ['product'],
};
</script>

<style>
/* стили для продукта */
</style>
