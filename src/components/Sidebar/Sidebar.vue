<template>
    <aside 
    class="flex flex-col bg-gray-800 text-white overflow-hidden min-h-screen p-4" 
    :class="`${collapsed ? 'w-80' : 'w-16'}`"
    >

        <div class="logo mb-4">
            <img class="w-8" src="../../assets/logo.svg" alt="">
        </div>

        <div 
        class="menu-toggle-wrap relative flex justify-end mb-4 "
        :class="`${collapsed ? '-top-12' : 'top-0'}`"
        >
            <button 
            class="menu-toggle transition hover:translate-x-2 hover:text-gray-400" 
            :class="`${collapsed ? 'rotate-180' : ''}`"
            @click="toggleMenu"
            >
                <font-awesome-icon class="text-xl" icon="fa-solid fa-angles-right" />
            </button>
        </div>
    </aside>    
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const collapsed = ref(false);


const toggleMenu = () => {
    collapsed.value = !collapsed.value
}
</script>

<style scoped>

aside {
    transition: 0.2s ease-out;
}

.menu-toggle-wrap {
    transition: 0.2s ease-out;
}


@media (max-width: 768px) {
    aside {
        position: fixed;
        z-index: 999;
    }
}
</style>