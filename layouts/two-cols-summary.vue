<script setup lang="ts">
const props = defineProps({
  class: {
    type: String,
  },
});
</script>

<template>
  <div class="slidev-layout two-columns w-full h-full">
    <div class="col-heading" :class="props.class">
        <slot name="heading" />
    </div>
    <div class="grid grid-cols-2">
      <div class="col-left" :class="props.class">
        <slot name="left" />
      </div>
      <div class="col-right" :class="props.class">
        <slot name="right" />
      </div>
      <div class="col-summary" :class="props.class">
        <slot name="summary" />
      </div>
    </div>
  </div>
</template>
