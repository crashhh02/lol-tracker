<template>
    <aside 
    class="flex flex-col bg-gray-800 text-white overflow-hidden min-h-screen p-2" 
    :class="`${collapsed ? 'collapsed w-80' : 'w-16'}`"
    >
    <div class="logo">
        <h1 class="text-xl" >LS</h1>
    </div>

    <div class="flex px-1 items-center mt-4" @click="toggleMenu">
        <font-awesome-icon class="text-xl" icon="fa-solid fa-angles-right" />
    </div>

    <div class="flex flex-col gap-4 mt-4 transition-all">
        <RouterLink class=" rounded hover:bg-slate-700 flex items-center justify-center p-2" to="/about">
            <font-awesome-icon class="text-xl" icon="fa-solid fa-home" />
            <span v-if="collapsed" class="text ml-4">About</span>
        </RouterLink>
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
    position: fixed;
        z-index: 999;
}




</style>