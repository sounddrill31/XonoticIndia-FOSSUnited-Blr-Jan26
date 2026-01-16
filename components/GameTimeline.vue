<script setup lang="ts">
interface TimelineItem {
  year: string
  title: string
  description?: string
}

defineProps<{
  items: TimelineItem[]
}>()
</script>

<template>
  <div class="ml-4 mt-2 font-sans max-h-[450px] pr-2 custom-scrollbar">
    <div 
      v-for="(item, idx) in items" 
      :key="idx" 
      class="relative pl-6 pb-3 last:pb-0" 
      v-click
    >
      <div 
        v-if="idx !== items.length - 1" 
        class="absolute left-[9px] top-2 h-full w-[2px] bg-gray-500/30"
      ></div>

      <div class="absolute left-0 top-1.5 h-5 w-5 rounded-full border-[3px] border-gray-900 bg-teal-500 shadow-[0_0_8px_rgba(20,184,166,0.6)]"></div>

      <div class="flex flex-col">
        <span class="text-base font-bold text-teal-400 font-mono leading-none mb-0.5">
          {{ item.year }}
        </span>
        <h4 class="text-base font-bold text-gray-100 leading-tight mb-0.5">
          {{ item.title }}
        </h4>
        <p v-if="item.description" class="text-xs text-gray-400 leading-snug opacity-90">
          {{ item.description }}
        </p>
      </div>
    </div>
  </div>
</template>

