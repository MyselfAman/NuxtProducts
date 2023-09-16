<template>
    <div>
       <nav class="nav">
        <NuxtLink class="text-2xl" to="/">Nuxt Dojo</NuxtLink>
        <ul class="navbarMenu">
            <li class="navbarLink"><NuxtLink to="/">Home</NuxtLink></li>
            <li class="navbarLink"><NuxtLink to="/about">About</NuxtLink></li>
            <li class="navbarLink"><NuxtLink to="/products">Products</NuxtLink></li>
        </ul>
       </nav>
       <div>
            <slot/>
       </div>
    </div>
 
</template>

<style >

.router-link-exact-active{
    color: #5CFF5C;
}

.nav{
    display: flex;
    flex-direction: space-between;
}

.nav ul li {
    display: flex;
    flex-direction: space-between;
}


</style>