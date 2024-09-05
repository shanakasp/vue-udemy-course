<template>
  <div>
    <h1>Child Slot</h1>

    <h2>{{ data }}</h2>

    <!-- Default slot for general content -->
    <div>
      <slot>Default content if nothing is provided</slot>
    </div>

    <!-- Named slot for strings -->
    <div>
      <h2>String Slot</h2>
      <slot name="string"></slot>
    </div>

    <!-- Named slot for numbers -->
    <div>
      <h2>Number Slot</h2>
      <slot name="number"></slot>
    </div>

    <!-- Named slot for images -->
    <div>
      <h2>Image Slot</h2>
      <slot name="image"></slot>
    </div>
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
