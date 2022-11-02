<!-- Отдельная "плитка" экскурсии -->
<template>
  <artice class="tile d-flex flex-column pa-4">
    <h1 class="tile__name">{{ name }}</h1>
    <TagList class="tile__tag-list" :info="info" />
  </artice>
</template>

<script>
import TagList from './TagList.vue';

export default {
  name: 'Tile',
  props: {
    name: String,
    info: Array,
  },
  components: {
    TagList,
  },
};
</script>

<style lang="scss" scoped>
.tile {
  gap: 0.5rem;
  border-bottom: 1px solid #bbb;
  width: 100vw;
}

.tile__name {
  cursor: pointer;
}
</style>
