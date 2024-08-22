<template>
    <product :product="product_data"></product>
</template>

<script>
import Product from "./Product.vue";
export default {
    name: "App",
    components: {Product},
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
