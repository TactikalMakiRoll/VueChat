<template>
    <div class="text-center py-8 px-8 relative">
        <button @click="closeInfo" class="absolute right-7 top-7 p-2 bg-gradient-to-br rounded-full from-[#3a69ec] to-[#144cb4] hover:bg-gradient-to-br hover:from-[#a142ee] hover:to-[#4230a8]">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
        </button>
        <div>
            <div class="space-y-2">
                <img class="w-17 mx-auto my-0" src="../assets/profile-image.png" alt="profile picture">
                <h2 class="text-xl font-bold">Steve Williams</h2>
                <h3 class="text-lg text-gray-20">Paris, France</h3>
                <p>Lorum ipsum blah blah blah blah blah blah blahb blahb bhal balh lbahs</p>
            </div>
            <div class="my-4 py-8 border-y-2 border-slate-700">
                <div>
                    <h3 class="inline-block font-bold text-gray-500 mr-2">Phone:</h3>
                    <span>+390 9385930585</span>
                </div>
                <div>
                    <h3 class="inline-block font-bold text-gray-500 mr-2">E-mail:</h3>
                    <span>sample@email.columns-md</span>
                </div>
            </div>
            <div></div>
        </div>
    </div>
</template>

<script setup>

const emit = defineEmits(['closeInfo']);

function fillSVG(e){
    e.target.childNodes[0].childNodes[0].setAttribute("fill","white");
};

function drainSVG(e){
    e.target.childNodes[0].childNodes[0].setAttribute("fill","none");
};

function closeInfo(){
    emit('closeInfo');
}

</script>

<style>

</style>