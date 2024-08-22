<template>
    <product-catalog></product-catalog>
</template>

<script>
import ProductCatalog from "./ProductCatalog.vue";
export default {
    name: "App",
    components: {
        ProductCatalog
    },
    data()  {
        return {
            product_data: {
                name: 'Товар 1',
                description: 'Описание товара 1',
                price: '1000'
            }
        }
    }
}
</script>

<style scoped>

</style>
