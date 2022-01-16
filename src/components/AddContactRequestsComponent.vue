<template>
  <div class="overflow-scroll scrollbar-hide h-full">
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
import { XCircleIcon, CheckCircleIcon } from '@heroicons/vue/solid'
import UserContactComponent from '@/components/User/UserContactComponent'

export default {
  name: 'AddContactRequestsComponent',
  components: {
    UserContactComponent,
    XCircleIcon,
    CheckCircleIcon
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
