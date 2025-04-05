<script setup>
import LinkItem from './LinkItem.vue'

const props = defineProps(['activeLink'])
const emit = defineEmits(['update:activeLink'])

const links = [
  { name: "POČETNA", active: true },
  { name: "SLIKA", active: true },
  { name: "ZVUK", active: false },
  { name: "GRAFIKA", active: true },
  { name: "MODEL", active: false },
  { name: "VIDEO", active: false }
]
</script>

<template>
  <nav class="sticky top-0 w-full flex gap-4 flex-wrap items-center justify-around bg-[#070F2B]/25 backdrop-blur-sm py-2 px-8 rounded-lg">
    <LinkItem 
      v-for="link in links"
      :key="link.name"
      :link="link"
      :activeLink="activeLink"
      @update:activeLink="emit('update:activeLink', $event)"
    />
  </nav>
</template>


