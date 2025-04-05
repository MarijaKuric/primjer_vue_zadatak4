<script setup>
const props = defineProps(['link', 'activeLink'])
const emit = defineEmits(['update:activeLink'])

const handleClick = () => {
  if (props.link.active) {
    emit('update:activeLink', props.link.name)
  }
}
</script>

<template>
  <div
    class="text-sm z-10 relative transition cursor-pointer"
    @click="handleClick"
    :class="[
      link.name === activeLink ? 'underline text-purple-100' : 'text-indigo-300 hover:text-indigo-200 hover:scale-105',
      link.active ? '' : 'text-indigo-500/50 pointer-events-none line-through'
    ]"
  >
    {{ link.name }}
    <b
      v-if="link.name === activeLink"
      class="text-purple-400 z-[-5] absolute -left-0.5 blur-md"
    >
      {{ link.name }}
    </b>
  </div>
</template>



