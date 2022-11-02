<template>
  <div class="tag-list__indicator d-flex flex-row">
    <v-icon v-if="!isFirstIndex" class="tag-list__indicator-divider"
      >mdi-circle-small</v-icon
    >

    <v-icon
      v-if="iconName"
      class="tag-list__indicator-icon text-grey-darken-1"
      >{{ iconName }}</v-icon
    >

    <span v-if="text" class="tag-list__indicator__text text-grey-darken-1">{{
      text
    }}</span>
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
