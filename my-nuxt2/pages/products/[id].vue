<template>
  <div>
    <Head>
      <Title>Online CD Store | {{ product.performer }}</Title>
      <!-- <Meta name="Album" :content="product.album" /> -->
    </Head>
    
    <ProductDetails :product="product" />
  </div>
</template>

<script setup>
  const { id } = useRoute().params
  const uri = 'https://fuzik03.tetraserver.com/compactdisc?album=' + id

  //  fetch the products
  
  const { data: product } = await useFetch(uri, { key: id })
  //const { data: product } = await useFetch(uri)
  //console.log(product.album);

  if (!product.value) {
    throw createError({ statusCode: 404, statusMessage: 'Product not found' })
  }

  definePageMeta({
    layout: "products",
  })
</script>