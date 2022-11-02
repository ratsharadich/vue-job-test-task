<!-- Список тэгов экскурсии -->
<template>
  <div class="tag-list d-flex flex-row flex-wrap overflow-y-hidden">
    <Tag
      class="tag-list__tag"
      v-for="(item, index) of info"
      :key="item?.value"
      :text="item?.value"
      :iconName="item?.iconName"
      :isFirstIndex="index === 0"
    />
  </div>
</template>

<script>
import Tag from './Tag.vue';

export default {
  name: 'TagList',
  props: {
    info: Array,
  },
  components: {
    Tag,
  },
};
</script>

<style lang="scss" scoped>
.tag-list {
  max-width: 100%;
  height: 24px;
}
</style>
