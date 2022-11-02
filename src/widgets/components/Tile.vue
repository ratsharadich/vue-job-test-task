<template>
  <artice class="tile d-flex flex-column pa-4">
    <h1 class="tile__name">{{ name }}</h1>

    <div class="tag-list d-flex flex-row flex-wrap overflow-y-hidden">
      <Tag
        v-for="(item, index) of info"
        :key="item?.value"
        :text="item?.value"
        :iconName="item?.iconName"
        :isFirstIndex="index === 0"
      />
    </div>
  </artice>
</template>

<script>
import Tag from './Tag.vue';

export default {
  name: 'Tile',
  props: {
    name: String,
    info: Array,
  },
  components: {
    Tag,
  },
};
</script>
