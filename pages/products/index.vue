<template>
  <div>
    <div class="grid grid-cols-auto gap-2 justify-center sm:grid-cols-[repeat(auto-fit,minmax(300px,1fr))]">
      <div v-for="p in products">
        <productCard :product="p"/>
      </div>
    </div>
  </div>
</template>

<script setup>
  definePageMeta({
    layout: "products",
  })

  //  fetch the products
  const { data: products } = await useFetch('https://fakestoreapi.com/products')

  useHead({
    title: 'Nuxt Dojo | Merch',
    meta: [
      { name: 'description', content: 'Nuxt 3 Merch'}
    ]
  })
</script>