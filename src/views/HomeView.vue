<script setup>
import HomeCard from '@/components/HomeCard.vue';
</script>

<template>
    <div class="p-8">
        <button
            type="button"
            class="text-white text-2xl font-semibold hover:underline cursor-pointer"
        >
            Podcast to make you smarter
        </button>

        <div class="py-1.5"></div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4">
            <HomeCard 
                image="https://picsum.photos/id/20/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />

            <HomeCard 
                image="https://picsum.photos/id/25/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />

            <HomeCard 
                image="https://picsum.photos/id/30/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />

            <HomeCard 
                image="https://picsum.photos/id/35/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />
        </div>
    </div>
    
    <div class="p-8">
        <button
            type="button"
            class="text-white text-2xl font-semibold hover:underline cursor-pointer"
        >
            Recomended Radio
        </button>

        <div class="py-1.5"></div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4">
            <HomeCard 
                image="https://picsum.photos/id/20/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />

            <HomeCard 
                image="https://picsum.photos/id/25/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />

            <HomeCard 
                image="https://picsum.photos/id/30/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />

            <HomeCard 
                image="https://picsum.photos/id/35/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />
        </div>
    </div>

    <div class="p-8">
        <button
            type="button"
            class="text-white text-2xl font-semibold hover:underline cursor-pointer"
        >
            Recomended Songs
        </button>

        <div class="py-1.5"></div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4">
            <HomeCard 
                image="https://picsum.photos/id/20/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />

            <HomeCard 
                image="https://picsum.photos/id/25/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />

            <HomeCard 
                image="https://picsum.photos/id/30/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />

            <HomeCard 
                image="https://picsum.photos/id/35/300/300" 
                title="Title is here" 
                subTitle="Subtitle is here"
            />
        </div>
    </div>
</template>
