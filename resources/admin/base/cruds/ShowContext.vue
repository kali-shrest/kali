<template>
  <div>
    <slot :title="getTitle" />
  </div>
</template>

<script lang="ts" setup>
  import { pageWithItemProps, pageWithItemSetup } from '@admin/mixins/pages'

  const props = defineProps(pageWithItemProps)

  const { getTitle } = pageWithItemSetup(props, 'show', 0)
</script>
