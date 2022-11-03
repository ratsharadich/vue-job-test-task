<!-- Конкретный тэг экскурсии -->
<template>
  <div class="tag d-flex flex-row flex-grow-0">
    <v-icon v-if="!isFirstIndex" class="tag-list__indicator-divider"
      >mdi-circle-small</v-icon
    >

    <div class="tag__elements d-flex flex-row">
      <v-icon v-if="iconName" class="tag__icon text-grey-darken-1">{{
        iconName
      }}</v-icon>

      <span v-if="text" class="tag__text text-grey-darken-1">{{ text }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Tag',
  props: {
    text: String || undefined,
    iconName: String || undefined,
    isFirstIndex: Boolean || undefined,
  },
};
</script>

<style lang="scss" scoped>
.tag__elements {
  gap: 0.25rem;
}

.tag__text {
  white-space: pre;
}
</style>
