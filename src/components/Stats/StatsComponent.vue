<script setup lang="ts">
const stats = [
  { id: 1, name: 'Post impression', stat: '1088' },
  { id: 2, name: 'Growth', stat: '+19.1%' },
  { id: 3, name: 'Profil view', stat: '+7%' },
]
</script>
<template>
  <div class="px-2">
    <p tabindex="0" class="text-lg font-bold font-heading text-primary">LinkedIn last 7 days</p>
    <dl class="mt-4 grid grid-cols-1 gap-5 md:grid-cols-3">
      <div
        v-for="item in stats"
        :key="item.name"
        class="overflow-hidden rounded-lg bg-card px-4 py-5 shadow sm:p-6 ring-1 ring-hover transition-all duration-300 ease-in-out transform hover:scale-105"
      >
        <dt tabindex="0" class="font-body truncate text-sm font-medium text-white-500">
          {{ item.name }}
        </dt>
        <dd
          tabindex="0"
          :style="{ color: item.id === 2 || item.id === 3 ? '#1FD8A4' : '' }"
          class="mt-1 text-3xl font-semibold font-heading tracking-tight text-white-900"
        >
          {{ item.stat }}
        </dd>
      </div>
    </dl>
  </div>
</template>
