<template>
    <div>
       <div v-for="product in products" :key="product.id" class="productDashboard">  
            <div class="card">
                <NuxtLink class="pt-4 text-[#5CFF5C]" :to="`/products/${product.id}`">{{ product.title }}</NuxtLink>
            </div>
       </div>
    </div>
</template>

<script setup>

    definePageMeta({
        layout : 'products'
    })

    const { data : products} = await useFetch('https://fakestoreapi.com/products');

</script>