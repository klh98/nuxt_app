<template>
    <div>
        <header class="shadow-sm bg-white">
           <nav class="container mx-auto p-4">
            <NuxtLink to="/products">Nuxt App</NuxtLink>
           </nav>
        </header>

        <!-- output the page content  -->
        <div class="container mx-auto p-4">
            <slot/>
        </div>

        <footer class="container mx-auto p-4 flex justify-between border-t-2">
            <nav>
                <ul class="flex gap-4">
                    <li><NuxtLink to="/">Home</NuxtLink></li>
                    <li><NuxtLink to="/about">About</NuxtLink></li>
                    <li><NuxtLink to="/products">Product</NuxtLink></li>
                </ul>
            </nav>
        </footer>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
.router-link-exact-active{
    color: #12b488;
}
</style>