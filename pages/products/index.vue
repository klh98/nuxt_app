<template>
    <div>
      <div class="grid grid-cols-4 gap-5">
        <div v-for="p in products" :key="p.id">
            <!-- <NuxtLink :to="`/products/${p.id}`">{{p.title}}</NuxtLink> -->

            <ProductCard :product="p"></ProductCard>
        </div>
      </div>
    </div>
</template>

<script setup>
    definePageMeta({
        layout: 'products'
    })

    // fetch the products 
    const { data:products } = await useFetch('https://fakestoreapi.com/products')
</script>

<style lang="scss" scoped>

</style>