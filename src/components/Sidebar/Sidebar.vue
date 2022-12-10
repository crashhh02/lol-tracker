<template>
    <aside class="flex flex-col bg-purple-800 text-white overflow-hidden min-h-screen p-4">

        <div class="logo mb-4">
            <img class="w-8" src="../../assets/logo.svg" alt="">
        </div>

        <div class="menu-toggle-wrap">
            <button class="menu-toggle">
                
            </button>
        </div>
    </aside>    
</template>

<script lang="ts" setup>
let sidebar_width = 300;
</script>

<style scoped>

aside {
    width: calc(2rem + 32px);
    transition: 0.2s ease-out;
}

@media (max-width: 768px) {
    aside {
        position: fixed;
        z-index: 999;
    }
}
</style>