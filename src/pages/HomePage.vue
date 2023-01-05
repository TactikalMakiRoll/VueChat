<template>
  <div class="w-full">
    <header-bar></header-bar>
    <navigation-bar></navigation-bar>
    <main>
      <div>
        <section class="px-4 pt-6 pb-3 flex border-y-2 border-slate-800 w-full" v-for="chat in chats" :key="chat.id">
          <img class="w-14" :src="getImgUrl(chat)" alt="profile pic">
          <div class="flex justify-between ml-5 grow">
            <div>
              <h3 class="text-lg">{{ chat.name }}</h3>
              <p class="text-[#6C7B8A] font-me">{{ chat.message }}</p>
            </div>
            <div class="">
              <p class="px-2 py-[2px] rounded-md bg-gradient-to-br from-[#5d27db] to-[#1d8eeb] font-thin">{{chat.last_date}}</p>
            </div>
          </div>
        </section>
      </div>
    </main>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import NavigationBar from '../components/UI/NavigationBar.vue';
import HeaderBar from '../components/UI/HeaderBar.vue';

const chats = ref([]);

for (let i = 0; i < 8; i++) {
  chats.value.push({
    name: "Jannet",
    avatar: "profile-image.png",
    message: "Are you free tonight?",
    last_date: "07:33AM",
  })
}

function getImgUrl(chat) {
    return new URL(`../assets/${chat.avatar}`, import.meta.url).href
}

</script>


<style>


</style>