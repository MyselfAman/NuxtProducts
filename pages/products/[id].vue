<template>
    <div class="mx-12 my-12">
       <div style="display:flex ">
        <div>
            <img style="border: 1px solid #5CFF5C" class="p-1" :src="product.image" alt="" height="50" width="300">
        </div>
        <div class="mx-20">
            <p class="text-2xl text-[#5CFF5C]">{{ product.title }}</p>
            <p class="pt-4">Description : {{ product.description }}</p>
            <p class="pt-4">Price : {{ product.price }}</p>
            <p class="pt-4">Rating {{ product.rating.rate }}</p>
        </div>

       </div>
    </div>
</template>

<script setup>
    const { id } = useRoute().params;

    definePageMeta({
        layout : 'products'
    })

    const url = 'https://fakestoreapi.com/products/' + id

    const { data : product} = await useFetch(url , {key:id})

    if(!product.value){
        throw createError({statusCode : 404 , statusMessage : 'Product not Found'})
    }


</script>