<template>
  <div class="w-full">
    <navigation-bar class="hidden"></navigation-bar>
    <main>
      <chat-feed class="hidden" :feed-array="chats"></chat-feed>
      <chat-window></chat-window>
    </main>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import NavigationBar from '../components/UI/NavigationBar.vue';
import ChatFeed from '../components/ChatFeed.vue';
import ChatWindow from '../components/ChatWindow.vue';

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