<script lang="ts" setup>
useSeoMeta({
  twitterSite: '@unjsio',
})

useSchemaOrg([
  defineWebSite({
    potentialAction: [
      defineSearchAction({ target: '/search?q={search_term_string}' }),
    ],
  }),
])
</script>

<template>
  <Html>
    <Body class="font-sans dark:bg-gray-900">
      <NuxtLoadingIndicator color="#ECDC5A" />

      <AppHeader />

      <div class="px-4 container mx-auto xl:max-w-7xl">
        <NuxtPage />
      </div>

      <AppFooter />

      <UNotifications />
    </Body>
  </Html>
</template>
