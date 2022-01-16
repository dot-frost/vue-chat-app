<template>
  <transition name="fade">
    <div class="h-screen w-screen absolute top-0 left-0" v-if="showPopup">
      <div class="absolute top-[15%] left-1/2 transform -translate-x-1/2 border border-slate-900 p-5 bg-slate-700 text-slate-100 min-w-[400px] z-50 shadow-2xl shadow-slate-900 flex flex-col gap-3 max-h-[60vh]">
        <header class="relative flex justify-between">
          <div class="flex-grow">
            {{ title }}
          </div>
          <button class="w-7">
            <XCircleIcon class="w-full" @click="closePopup"/>
          </button>
        </header>
        <hr/>
        <slot/>
      </div>
    </div>
  </transition>
</template>

<script>
import { XCircleIcon } from '@heroicons/vue/solid'

export default {
  name: 'PopupComponent',
  props: {
    title: {
      required: true
    },
    show: {
      required: true
    }
  },
  components: {
    XCircleIcon
  },
  data () {
    return {
      status: false
    }
  },
  created () {
    this.status = this.show
  },
  updated () {
    this.status = this.show
  },
  computed: {
    showPopup () {
      return this.status & this.show
    }
  },
  methods: {
    closePopup () {
      this.status = false
      this.$emit('close_popup')
    }
  }
}
</script>

<style scoped>

</style>
