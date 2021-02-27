<template>
  <div class="flex space-x-4">
    <div v-if="!short">
      <div class="flex-col hidden w-24 text-right md:flex md:min-w-min">
        <span class="text-sm font-medium">{{ fullName }}</span>
        <span class="text-xs truncate"> {{ job }} </span>
      </div>
    </div>
    <div
      class="relative flex-shrink-0 w-8 h-8 text-white bg-yellow-400 rounded-full shadow-lg flex justify-center items-center ring-2 ring-white"
    >
      <div
        role="present"
        class="absolute top-0 right-0 w-2 h-2 uppercase bg-green-500 rounded-full shadow-md ring-white ring-1"
      />
      {{ shortenName() }}
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    fullName: { type: String, default: '' },
    job: { type: String, default: '' },
    short: { type: Boolean, default: false },
  },
  methods: {
    shortenName() {
      return [...this.fullName.split(' ')].map((element) => element[0]).join('')
    },
  },
})
</script>

<style></style>
