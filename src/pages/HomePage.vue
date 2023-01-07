<template>
  <div class="w-full">
    <navigation-bar class="hidden"></navigation-bar>
    <main class="flex">
      <chat-feed class="hidden" :feed-array="chats"></chat-feed>
      <chat-window class="border-2 border-slate-800 max-w-3xl md:max-w-lg"></chat-window>
      <chat-info></chat-info>
    </main>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import NavigationBar from '../components/UI/NavigationBar.vue';
import ChatFeed from '../components/ChatFeed.vue';
import ChatWindow from '../components/ChatWindow.vue';
import ChatInfo from '../components/ChatInfo.vue';

const chats = ref([]);

for (let i = 0; i < 8; i++) {
  chats.value.push({
    name: "Jannet",
    avatar: "profile-image.png",
    message: "Are you free tonight?",
    last_date: "07:33AM",
  })
}


</script>


<style>


</style>