<script setup lang="ts">
// eslint-disable-next-line @typescript-eslint/prefer-ts-expect-error
// @ts-ignore tsconfig
import { NuxtLink } from '#components'

const props = defineProps<{
  to?: string
  icon: string
  disabled?: boolean
}>()
</script>

<template>
  <Component
    :is="to ? NuxtLink : 'button'"
    :to="to"
    v-bind="$attrs"
    class="n-transition n-icon-button"
    :class="{
      'n-disabled op10!': props.disabled,
    }"
  >
    <NIcon :icon="props.icon" />
  </Component>
</template>
