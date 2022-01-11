<template>
  <div class="flex justify-start px-5 py-3 gap-2 items-center cursor-pointer">
    <AvatarComponent :image="user.avatar"
                     :alt="user.full_name"
                     :status="user.status"
                     :status-type="statusType"
                     class="w-12"/>
    <div class="hidden md:block">
      <h3 class="">{{ user.full_name }}</h3>
      <p class="text-sm" v-if="latest">{{ latest }}</p>
    </div>
  </div>
</template>

<script>
import AvatarComponent from '@/components/User/AvatarComponent'
export default {
  name: 'UserContactComponent',
  components: { AvatarComponent },
  props: {
    user: {
      required: true
    },
    latest: {
      default: false
    },
    statusType: {
      required: true
    }
  }
}
</script>

<style scoped>

</style>
