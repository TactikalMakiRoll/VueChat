<template>
    <div class="h-screen">
        <div class="relative px-4 sticky flex justify-between top-0 w-full py-7 border-b-2 border-slate-800 bg-[rgba(6,27,45,1)]">
            <div class="flex">
                <img class="w-14 h-14 aspect-square mr-2" src="../assets/profile-image.png" alt="profile pic">
                <div>
                    <h2 class="font-bold">Steve Williams</h2>
                    <span class="text-gray-400 whitespace-nowrap">Last seen 3 hours ago</span>
                </div>
            </div>
            <div class="flex flex-nowrap">
                <button @mouseleave.self="drainSVG($event)" @mouseenter.self="fillSVG($event)" class="p-1">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z" />
                    </svg>
                </button>
                <button @mouseleave.self="drainSVG($event)" @mouseenter.self="fillSVG($event)" class="p-1">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                        <path stroke-linecap="round" d="M15.75 10.5l4.72-4.72a.75.75 0 011.28.53v11.38a.75.75 0 01-1.28.53l-4.72-4.72M4.5 18.75h9a2.25 2.25 0 002.25-2.25v-9a2.25 2.25 0 00-2.25-2.25h-9A2.25 2.25 0 002.25 7.5v9a2.25 2.25 0 002.25 2.25z" />
                    </svg>
                </button>
                <button @mouseleave.self="drainSVG($event)" @mouseenter.self="fillSVG($event)" class="p-1">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M6.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM12.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM18.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
                    </svg>
                </button>
            </div>
        </div>
        <div class="px-4 pt-5 flex flex-col space-y-5 justify-end">
            <div class="inline-block flex-none px-4 pt-2 pb-4 bg-blue-800 rounded-3xl drop-shadow-lg ">
                <pre>Hi Alex! What's Up?</pre>
            </div>
            
            <div>
                <pre>Oh, hello! All perfectly.</pre>
            </div>
            
            <div>
                <pre>Hi Alex! What's Up?</pre>
            </div>
            
            <div>
                <pre>Hi Alex! What's Up?</pre>
            </div>
        </div>
        <div class="px-3 py-3 w-full flex fixed bottom-0 border-t-2 border-slate-800">
            <input placeholder="Write your message..." class="italic grow bg-slate-800 rounded-sm mr-3 py-2 pl-2 placeholder:italic placeholder:text-slate-400" type="text" name="message" id="message">
            <button class="p-2 rounded-full bg-purple-800">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M6 12L3.269 3.126A59.768 59.768 0 0121.485 12 59.77 59.77 0 013.27 20.876L5.999 12zm0 0h7.5" />
                </svg>
            </button>
        </div>
    </div>
</template>

<script setup>
    function fillSVG(e){
        e.target.childNodes[0].childNodes[0].setAttribute("fill","white");
        console.log(e.target);
    };
    
    function drainSVG(e){
        e.target.childNodes[0].childNodes[0].setAttribute("fill","none");
    };
</script>

<style>

</style>