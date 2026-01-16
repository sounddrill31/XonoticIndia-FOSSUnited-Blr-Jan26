<script setup lang="ts">
interface TimelineItem {
  year: string
  title: string
}

defineProps<{
  items: TimelineItem[]
}>()
</script>

<template>
  <div class="relative w-full font-sans mt-16">
    
    <div class="absolute left-0 top-3 w-full h-3 bg-green-500/80 rounded-full"></div>

    <div class="relative flex justify-between items-start">
      <div 
        v-for="(item, idx) in items" 
        :key="idx" 
        class="flex flex-col items-center flex-1"
      >
        
        <div class="relative z-10">
          <div class="w-8 h-8 rounded-full border-4 border-green-500/90 bg-green-200 shadow-md"></div>
        </div>
<br>
<br>
        <div class="mt-8 transform -rotate-45 origin-top-left text-left">
          
          <div class="text-sm font-bold text-green-800 font-mono tracking-tight">
            {{ item.year }}
          </div>
          
          <h4 class="text-base font-bold text-white-800 leading-tight">
            {{ item.title }}
          </h4>
          
        </div>

      </div>
    </div>

  </div>
</template>