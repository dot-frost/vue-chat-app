<template>
  <div class="bg-gray-200 h-screen max-h-screen min-h-screen flex justify-center items-center px-10 py-20">
    <div class="max-w-screen-lg flex-grow h-full overflow-hidden flex flex-coll justify-items-stretch items-stretch">
      <!-- Sidebar -->
      <div id="sidebar" class="bg-slate-700 flex flex-col justify-items-stretch text-white w-20 md:w-[300px]">
        <!-- Profile -->
        <div class="flex items-center p-4 md:p-9 gap-4">
          <AvatarComponent :image="require('@/assets/images/person/haroldgunderson.png')"
                           alt="Ali Talebi"
                           status="online"
                           status-type="circle"
                           class="w-16"/>
          <h2 class="w-full hidden md:block">Mike Rose</h2>
          <ChevronDownIcon class="w-10 hidden md:block"/>
        </div>
        <!-- Search -->
        <div class="border-y border-slate-600 relative hidden md:block">
          <SearchIcon class="w-10 h-10 p-2 absolute left-1"/>
          <input type="text" class="bg-slate-600 outline-0 pl-12 placeholder-white h-9 w-[17.2em]"
                 placeholder="Search contact...">
        </div>
        <!-- Contacts -->
        <div class="flex flex-grow overflow-auto flex-col scrollbar-hide">
          <UserContactComponent
            :user="{ full_name: 'Ali Talebi' , avatar:require('@/assets/images/person/haroldgunderson.png') , status:'online'}"
            :latest="'Hello Word!!'"
            :status-type="'dot'"
            v-for="i in 20"
            :key="i"
          />
        </div>
        <!-- Actions -->
        <div class="flex flex-col md:flex-row justify-evenly text-sm gap-0.5">
          <div
            class="flex bg-slate-600 w-full justify-center items-center gap-1 py-2 cursor-pointer hover:bg-slate-500">
            <UserAddIcon class="w-7 md:5"/>
            <span class="hidden md:block">Add contact</span>
          </div>
          <div
            class="flex bg-slate-600 w-full justify-center items-center  gap-1 py-2 cursor-pointer hover:bg-slate-500 group">
            <AdjustmentsIcon class="w-7 md:5"/>
            <span class="hidden md:block">Settings</span>
          </div>
        </div>
      </div>
      <!-- ChatBox -->
      <div class="flex-grow bg-white">
      </div>
    </div>
  </div>
</template>

<script>
import { ChevronDownIcon, SearchIcon, UserAddIcon, AdjustmentsIcon } from '@heroicons/vue/solid'
import AvatarComponent from '@/components/User/AvatarComponent'
import UserContactComponent from '@/components/User/UserContactComponent'

export default {
  name: 'HomeView',
  components: {
    UserContactComponent,
    AvatarComponent,
    ChevronDownIcon,
    SearchIcon,
    UserAddIcon,
    AdjustmentsIcon
  }
}
</script>
