<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <NuxtLink to="/" class="font-bold">Four Archons</NuxtLink>
                <ul class="flex gap-4">
                    <li><NuxtLink to="/">Home</NuxtLink></li>
                    <li><NuxtLink to="/barbatos" class="btn">Barbatos</NuxtLink></li>
                    <li><NuxtLink to="/morax" class="btn">Morax</NuxtLink></li>
                    <li><NuxtLink to="/beelzebub" class="btn">Beelzebub</NuxtLink></li>
                    <li><NuxtLink to="/buer" class="btn">Buer</NuxtLink></li>
                </ul>
            </nav>
        </header>

        <!-- page content go here -->
        <div class="container mx-auto p-4">
            <slot />
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
    .router-link-exact-active {
        color: #5602D4;
    }
</style>