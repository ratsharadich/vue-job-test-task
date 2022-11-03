<!-- Список тэгов экскурсии -->
<template>
  <div class="tag-list d-flex flex-row overflow-x-hidden">
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
  mounted() {
    window.addEventListener('resize', this.windowResizeEventHandler);
  },
  unmounted() {
    window.removeEventListener('resize', this.windowResizeEventHandler);
  },
  methods: {
    windowResizeEventHandler() {
      const container = document.querySelector('.tag-list');
      const items = document.querySelectorAll('.tag-list__tag');

      items.forEach((item) => {
        const containerOffset = container.offsetLeft + container.offsetWidth;
        const itemOffset = item.offsetLeft + item.offsetWidth;

        if (containerOffset < itemOffset) {
          item.style.visibility = 'hidden';
        } else {
          item.style.visibility = 'visible';
        }
      });
    },
  },
  components: {
    Tag,
  },
};
</script>

<style lang="scss" scoped>
.tag-list {
  max-width: 100%;
}
</style>
