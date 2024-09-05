<template>
  <div>
    <h1>Child Slot</h1>
    <h1>{{ data }}</h1>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "ChildSlot",
  props: {
    data: String,
  },
};
</script>

<style></style>
