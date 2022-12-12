
<template>
    <main class="bg-gray-900  min-h-screen">

        <div class="mt-32">
            <h1 class="text-white text-xxl font-bold text-center">Search your summoner name for the stats!</h1>
            <SearchSummoner/>
        </div>

    </main>       
</template>

<script setup lang="ts">
import SearchSummoner from '@/components/SearchSummoner.vue';
</script>

<style scoped>

    main {
      background-image: url('../assets/akshan_wallpaper.jpg');
      background-size: cover;
    }
</style>

