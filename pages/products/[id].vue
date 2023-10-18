<template>
    <div>
      <ProductDetail :product="product"></ProductDetail>
    </div>
</template>

<script setup>
  const {id} = useRoute().params
  const url = 'https://fakestoreapi.com/products' + id

    // fetch the products 
    const { data:product } = await useFetch(url, { key:id })

  definePageMeta({
    layout : 'products'
  })
</script>

<style lang="scss" scoped>

</style>