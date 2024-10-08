<script setup>
  const { setLocale } = useI18n()
</script>

<template>
  <div class="bg-stone-200 dark:bg-stone-950 min-h-screen w-full">
    <UButton @click="setLocale('en')">en</UButton>
    <UButton @click="setLocale('fr')">fr</UButton>
    <UCard>
      <template #header>
        <div class="h-8">{{ $t('welcome') }}</div>
      </template>
      <div class="h-16">{{ $t('message') }}</div>
      <template #footer>
        <div class="h-8">{{ $t('greeting.hello') }}</div>
      </template>
    </UCard>
    <UMeter :value="80" indicator label="Memory usage" />
  </div>
</template>