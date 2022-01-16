<template>
  <div class="overflow-scroll scrollbar-hide h-full">
    <div class="border-y border-slate-600 relative hidden md:block">
      <SearchIcon class="w-10 h-10 p-2 absolute left-1"/>
      <input type="text" class="bg-slate-600 outline-0 pl-12 placeholder-white h-9 w-full"
             placeholder="Search contact...">
    </div>
    <div class="flex gap-2 items-center" v-for="i in 50" :key="'requests_' + i">
      <UserContactComponent status-type="circle" :user="user" class="gap-5 flex-grow"/>
      <button class="w-10 bg-green-500 rounded-full">
        <CheckCircleIcon class="w-full"/>
      </button>
      <button class="w-10 bg-red-500 rounded-full">
        <XCircleIcon class="w-full"/>
      </button>
    </div>
  </div>
</template>

<script>

import { XCircleIcon, CheckCircleIcon, SearchIcon } from '@heroicons/vue/solid'
import UserContactComponent from '@/components/User/UserContactComponent'

export default {
  name: 'AddContactsSearchComponent',
  components: {
    UserContactComponent,
    XCircleIcon,
    CheckCircleIcon,
    SearchIcon
  },
  data () {
    return {
      user: {
        full_name: 'Ali Talebi',
        avatar: require('@/assets/images/person/haroldgunderson.png'),
        status: 'online'
      }
    }
  }
}
</script>

<style scoped>

</style>
