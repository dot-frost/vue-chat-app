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
        <!-- Contacts -->
        <!-- Actions -->
      </div>
      <!-- ChatBox -->
      <div class="flex-grow bg-white">
      </div>
    </div>
  </div>
</template>

<script>
import { ChevronDownIcon } from '@heroicons/vue/solid'
import AvatarComponent from '@/components/User/AvatarComponent'

export default {
  name: 'HomeView',
  components: {
    AvatarComponent,
    ChevronDownIcon
  }
}
</script>
