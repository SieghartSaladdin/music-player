<script setup>
import CategorySelect from '@/components/CategorySelect.vue';
</script>

<template>
    <div class="p-8">
        <button
            type="button"
            class="text-white text-2xl font-semibold hover:underline cursor-pointer"
        >
            Recomended Songs
        </button>

        <div class="py-1.5"></div>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-6">
            <CategorySelect 
                image="https://picsum.photos/id/40/300/300"
                category="Podcasts" 
            />
            <CategorySelect 
                image="https://picsum.photos/id/45/300/300"
                category="New Release" 
            />
            <CategorySelect 
                image="https://picsum.photos/id/50/300/300"
                category="Audio Books" 
            />
            <CategorySelect 
                image="https://picsum.photos/id/55/300/300"
                category="Anime Songs" 
            />
            <CategorySelect 
                image="https://picsum.photos/id/60/300/300"
                category="Mushoku Tensei" 
            />
            <CategorySelect 
                image="https://picsum.photos/id/36/300/300"
                category="Podcasts" 
            />
            <CategorySelect 
                image="https://picsum.photos/id/17/300/300"
                category="New Release" 
            />
            <CategorySelect 
                image="https://picsum.photos/id/19/300/300"
                category="Audio Books" 
            />
            <CategorySelect 
                image="https://picsum.photos/id/22/300/300"
                category="Anime Songs" 
            />
            <CategorySelect 
                image="https://picsum.photos/id/33/300/300"
                category="Mushoku Tensei" 
            />
        </div>
    </div>
</template>