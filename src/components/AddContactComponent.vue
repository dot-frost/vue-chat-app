<template>
  <div class="flex flex-col gap-3 overflow-scroll scrollbar-hide">
    <div class="flex justify-evenly gap-2">
      <button class="bg-slate-500 w-full py-2 hover:bg-slate-800" @click="setComponent('search')">Search</button>
      <button class="bg-slate-500 w-full py-2 hover:bg-slate-800" @click="setComponent('requests')">Requests</button>
    </div>
    <Component :is="activeComponent"/>
  </div>
</template>

<script>

import AddContactRequestsComponent from '@/components/AddContactRequestsComponent'
import AddContactsSearchComponent from '@/components/AddContactsSearchComponent'

export default {
  name: 'AddContactComponent',
  components: {
    AddContactsSearchComponent,
    AddContactRequestsComponent
  },
  data () {
    return {
      activeComponent: 'AddContactsSearchComponent'
    }
  },
  methods: {
    setComponent (component) {
      this.activeComponent = {
        search: AddContactsSearchComponent,
        requests: AddContactRequestsComponent
      }[component]
    }
  }
}
</script>

<style scoped>

</style>
