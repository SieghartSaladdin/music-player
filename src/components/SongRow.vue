<script setup>
import { ref, toRefs, onMounted } from 'vue';

import Play from 'vue-material-design-icons/Play.vue';
import Pause from 'vue-material-design-icons/Pause.vue';
import Heart from 'vue-material-design-icons/Heart.vue';


import { useSongStore } from '../stores/song'
import { storeToRefs } from 'pinia';
const useSong = useSongStore()
const { isPlaying, audio, currentTrack, currentArtist } = storeToRefs(useSong)

let isHover = ref(false);
let isTrackTime = ref(null);

const props = defineProps({
    track: Object,
    artist: Object,
    index: Number,
});

const { track, artist, index } = toRefs(props);

onMounted(() => {
    const audio = new Audio(track.value.path);
    audio.addEventListener('loadedmetadata', function() {
        const duration = audio.duration;
        const minutes = Math.floor(duration / 60);
        const seconds = Math.floor(duration % 60);
        isTrackTime.value = minutes+':'+seconds.toString().padStart(2, '0')
    });
});

</script>


<template>
    <li
        class="flex items-center justify-between rounded-md hover:bg-[#2a2929]"
        @mouseenter="isHover = true"
        @mouseleave="isHover = false"
    >
        <div class="flex items-center w-full py-1.5">
            <div v-if="isHover" class="w-[40px] ml-[14px] mr-[6px] cursor-pointer">
                <Play 
                    v-if="!isPlaying" 
                    fillColor="#ffffff" 
                    :size="25"
                    @click="useSong.playOrPauseThisSong(artist, track)"
                />
                <Play 
                    v-else-if="isPlaying && currentTrack.name !== track.name"
                    fillColor="#ffffff" 
                    :size="25"
                    @click="useSong.playOrPauseThisSong(artist, track)"
                />
                <Pause v-else fillColor="#ffffff" :size="25" @click="useSong.playOrPauseSong"/>
            </div>
            <div v-else class="text-white font-semibold w-[40px] ml-5">
                <span :class="{'text-green-500': currentTrack && currentTrack.name === track.name}">
                    {{ index }}
                </span>
            </div>
            <div>
                <div  
                    class="text-white font-semibold"
                >
                    <span :class="{'text-green-500': currentTrack && currentTrack.name === track.name}">
                        {{ track.name }}
                    </span>
                </div>
                <div class="text-sm font-semibold text-gray-400">{{ artist.name }}</div>
            </div>
        </div>

        <div class="flex items-center">
            <button type="button" v-if="isHover">
                <Heart fillColor="#1bd760" :size="22"/>
            </button>
            <div
                v-if="isTrackTime"
                class="text-xs mx-5 text-gray-500"
            >
                {{ isTrackTime }}
            </div>
        </div>
    </li>
</template>