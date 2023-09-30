<template>
  <section class="flex flex-col my-32 p-3">
    <h2
      v-if="title"
      class="mb-3 text-3xl text-5xl self-start sm:self-center"
      :class="titleAlignment"
    >
      {{ title }}
    </h2>
    <slot />
  </section>
</template>

<script>
export default {
  name: "BaseSection",
  props: {
    title: {
      type: String,
      default: "",
    },
    titleAlignment: {
      type: [String],
      default: "",
    },
  },
};
</script>

<style lang="scss" scoped></style>
