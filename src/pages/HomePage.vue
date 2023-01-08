<template>
  <div class="w-full max-w-[1920px] mx-auto border-x-2 border-slate-800">
    <navigation-bar class="hidden"></navigation-bar>
    <main class="flex">
      <chat-feed :class="{
                    hidden: !feedView,
                  }" 
                  class="w-full md:flex md:max-w-md border-2 md:border-0 border-slate-800" :feed-array="chats">
      </chat-feed>
      <chat-window  @toggle-info="toggleInfo" :class="{
                      hidden: feedView,
                    }" 
                    class="w-full border-2 max-w-screen-xl md:flex border-slate-800">
      </chat-window>
      <chat-info @close-info="toggleInfo" :class="{
          hidden: infoHiddenSize,
        }"
        >

      </chat-info>
    </main>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
import NavigationBar from '../components/UI/NavigationBar.vue';
import ChatFeed from '../components/ChatFeed.vue';
import ChatWindow from '../components/ChatWindow.vue';
import ChatInfo from '../components/ChatInfo.vue';

const chats = ref([]);
let feedView = ref(true);
let infoHidden = ref(true);
let currentFeed = ref(null);

for (let i = 0; i < 8; i++) {
  chats.value.push({
    name: "Jannet",
    avatar: "profile-image.png",
    message: "Are you free tonidwaaaaaaasght fdsaf afsd asd fs fdas fas df asd fasd fas fewa fsd a?",
    last_date: "07:33AM",
  })
}

const infoHiddenSize = computed(() => {
  if(!infoHidden.value && window.screen.width>=1024){
    return false;
  }
  return true;
})


function toggleInfo(){
  infoHidden.value = !infoHidden.value;
}

</script>


<style>


</style>