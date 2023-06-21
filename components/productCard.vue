<template>
    <div class="card text-center">
        <div>
        <img :src="product.image" alt="product thumb" class="thumb">

        </div>
        <p class="font-bold text-gray-500 truncate my-3">{{ product.title }}</p>
        <NuxtLink :to="`/products/${product.id}`" class="btn my-3">View Details</NuxtLink>
        
    </div>
</template>

<script setup>
const {product} = defineProps(['product'])
</script>

<style  scoped>
.thumb{
    max-height: 120px;
    max-width: 70%;
    margin: 0 auto;
}
</style>