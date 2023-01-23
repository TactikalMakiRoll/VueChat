<template>
    <div class="h-screen flex flex-col">
        <div class="px-4 justify-self-start flex justify-between top-0 w-full py-7 bg-[rgba(6,27,45,1)]">
            <h1 :class="{
                hidden: searchExpanded,
            }"
            class="inline-block font-semibold tracking-widest">FEED</h1>
            <button @click="searchExpanded = true" :class="{
                hidden: searchExpanded,
            }"
            class="inline-block tracking-widest">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 hover:text-[#3CA4F7]">
                <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
                </svg>
            </button>
            <input @focusout="searchExpanded = true" @keypress="checkCloseSearch($event)" class="grow-1 w-full italic grow bg-slate-800 rounded-sm mr-3 py-1 pl-2 placeholder:italic placeholder:text-slate-400" 
            :class="{
                hidden: !searchExpanded,
            }" type="text" name="searchfield" id="search">
        </div>
        <div class="overflow-scroll grow-0 scrollbar-hide">
            <section class="px-4 pt-6 pb-3 flex border-t-2 border-slate-800 w-full" v-for="chat in feedArray" :key="chat.id">
                <img class="h-14" :src="getImgUrl(chat)" alt="profile pic">
                <div class="flex justify-between ml-5 grow">
                <div>
                    <h3 class="text-lg">{{ chat.name }}</h3>
                    <p class="text-[#6C7B8A] font-me">{{ chat.message }}</p>
                </div>
                <div class="ml-3">
                    <p class="px-2 py-[2px] rounded-md bg-gradient-to-br from-[#5d27db] to-[#1d8eeb] font-thin">{{chat.last_date}}</p>
                </div>
                </div>
            </section>
        </div>
    </div>
</template>

<script setup>
    import {ref, defineProps} from 'vue';

    const searchExpanded = ref(false);

    const props = defineProps({
        feedArray: Array,
    })
    
    function getImgUrl(chat) {
        return new URL(`../assets/${chat.avatar}`, import.meta.url).href
    }

    function checkCloseSearch(event){
        if(event.key === "Enter" || event.key === "Escape"){
            searchExpanded.value = !searchExpanded.value;
        }
    }
</script>

<style>

</style>