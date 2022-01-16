<template>
  <div class="flex flex-col justify-start gap-3 overflow-scroll scrollbar-hide">
    <div class="w-2/6 mx-auto relative">
      <AvatarComponent status="" alt="Ali Talebi" :image="require('./../assets/images/person/harveyspecter.png')"
                       class="self-center"/>
      <button class="absolute w-10 bg-slate-500 rounded-full p-1.5 right-0.5 bottom-0.5 border-slate-700 border-4">
        <UploadIcon class="w-full"/>
      </button>
    </div>
    <div class="flex justify-evenly gap-3">
      <div class="">
        <input class="px-3 py-1.5 text-white placeholder-slate-400 bg-slate-500 w-full" placeholder="First Name">
      </div>
      <div class="">
        <input class="px-3 py-1.5 text-white placeholder-slate-400 bg-slate-500 w-full" placeholder="Last Name">
      </div>
    </div>
    <div class="">
      <input class="px-3 py-1.5 text-white placeholder-slate-400 bg-slate-500 w-full"
             placeholder="Your Email Address">
    </div>
    <div class="">
      <input class="px-3 py-1.5 text-white placeholder-slate-400 bg-slate-500 w-full" placeholder="New Password">
    </div>
    <div class="">
      <input class="px-3 py-1.5 text-white placeholder-slate-400 bg-slate-500 w-full"
             placeholder="Confirm New Password">
    </div>
    <button class="bg-slate-500 hover:bg-slate-800 w-32 py-2 px-5 mx-auto" @click="$emit('done')">Save</button>
  </div>
</template>

<script>
import { UploadIcon } from '@heroicons/vue/solid'
import AvatarComponent from '@/components/User/AvatarComponent'

export default {
  name: 'SettingsComponent',
  components: {
    AvatarComponent,
    UploadIcon
  }
}
</script>

<style scoped>

</style>
