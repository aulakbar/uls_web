<script setup lang="ts">
// https://github.com/vueuse/head
// you can use this to manipulate the document head in any components,
// they will be rendered correctly in the html results with vite-ssg
useHead({
  title: 'Ururu',
  meta: [
    { name: 'description', content: 'Aulia Akkbar Personal Website' },
  ],
  link: [
    {
      rel: 'icon',
      type: 'image/svg+xml',
      href: '/favicon/favicon-32x32.png',
    },
  ],
})
</script>

<template>
  <RouterView />
</template>
