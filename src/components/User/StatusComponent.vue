<template>
  <span class="rounded-full outline outline-offset-2 outline-3 w-full h-full absolute"
        v-if="type === 'circle'"
        :class="classList"
  ></span>
  <span v-else class="absolute bg-red-600 p-1 rounded-full border border-slate-700" :class="classList"></span>
</template>

<script>
export default {
  name: 'StatusComponent',
  props: {
    type: {
      required: true,
      type: String
    },
    color: {
      required: false,
      default: 'green',
      type: String
    }
  },
  computed: {
    classList () {
      const classes = {
        circle: {
          green: 'outline-green-500',
          blue: 'outline-blue-500',
          red: 'outline-red-500',
          yellow: 'outline-yellow-500',
          purple: 'outline-purple-500',
          gray: 'outline-gray-500',
          black: 'outline-black'
        },
        dot: {
          green: 'bg-green-500',
          blue: 'bg-blue-500',
          red: 'bg-red-500',
          yellow: 'bg-yellow-500',
          purple: 'bg-purple-500',
          gray: 'bg-gray-500',
          black: 'bg-black'
        }
      }
      return [
        classes[this.type][this.color]
      ]
    }
  }
}
</script>

<style scoped>

</style>
