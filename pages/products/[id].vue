<template>
    <div>
        <ProductDetails :product="product" />
    </div>
</template>

<script setup>
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id

//fetch the product
const { data: product } = await useFetch(uri)

if (!product.value){
    throw createError({ statusCode: 404, statusMessage: ' product not found'})
}

definePageMeta({
    layout: 'products'
})
</script>

<style scoped>

</style>