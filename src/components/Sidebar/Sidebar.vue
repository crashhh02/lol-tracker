<template>
    <aside 
    class="flex flex-col bg-gray-800 text-white overflow-hidden min-h-screen p-4" 
    :class="`${collapsed ? 'collapsed w-80' : 'w-16'}`"
    >

        <div class="logo mb-4">
            <img class="w-8" src="../../assets/logo.svg" alt="">
        </div>

        <div 
        class="menu-toggle-wrap relative flex  mb-4 "
        :class="`${collapsed ? '-top-12 justify-end' : 'top-0 justify-center'}`"
        >
            <button 
            class="menu-toggle transition hover:translate-x-2 hover:text-gray-400" 
            :class="`${collapsed ? 'rotate-180' : ''}`"
            @click="toggleMenu"
            >
                <font-awesome-icon class="text-xl" icon="fa-solid fa-angles-right" />
            </button>
        </div>

        <h3 class="transition leading-8 text-gray-500 font-bold text-sm mb-2"
        :class="`${collapsed ? 'opacity-1' : 'opacity-0'}`"
        >MENU</h3>
        <div class="menu my-0 -mx-4">

            <router-link class="button hover:bg-gray-700 hover:text-green-500" to="/">
                <font-awesome-icon class=" mr-4" icon="fa-solid fa-house" />
                <span class="text">Home</span>
            </router-link>

            <router-link class="button hover:bg-gray-700 hover:text-green-500" to="/">
                <font-awesome-icon class=" mr-4" icon="fa-solid fa-list-ul" />
                <span class="text">Home</span>
            </router-link>

            <router-link class="button hover:bg-gray-700 hover:text-green-500" to="/about">
                <font-awesome-icon class=" mr-4" icon="fa-solid fa-house" />
                <span class="text">About</span>
            </router-link>

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

.text {
    opacity: 0;
    transition: 0.3s ease-out;
}
.collapsed .text {
    opacity: 1;
}

.menu-toggle-wrap {
    transition: 0.2s ease-out;
}

.button {
    display: flex;
    align-items: center;
    text-decoration: none;
    padding: 0.5rem 1.5rem ;
    transition: 0.2s ease-out;

}


@media (max-width: 768px) {
    aside {
        position: fixed;
        z-index: 999;
    }
}
</style>