<template>
  <div class="rounded-full relative">
    <StatusComponent :type="statusType" :color="statusColor" v-if="status"/>
    <img :src="image" :alt="alt" class="w-full rounded-full">
  </div>
</template>

<script>
import StatusComponent from '@/components/User/StatusComponent'

export default {
  name: 'AvatarComponent',
  components: { StatusComponent },
  props: {
    image: {
      required: true
    },
    alt: {
      required: true
    },
    status: {
      default: false
    },
    statusType: {
      default: 'dot'
    }
  },
  computed: {
    statusColor () {
      return {
        online: 'green',
        offline: 'gray'
      }[this.status]
    }
  }
}
</script>

<style scoped>

</style>
