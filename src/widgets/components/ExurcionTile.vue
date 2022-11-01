<template>
  <artice class="excursion-tile">
    <h1>{{ name }}</h1>

    <div class="excursion-tile__info">
      <div>{{ rating }}</div>
      <div>{{ type }}</div>
      <div>{{ transport }}</div>
      <div>{{ date }}</div>
      <div>{{ duration }}</div>
    </div>
  </artice>
</template>

<script>
export default {
  name: 'ExcursionTile',
  props: {
    name: String,
    rating: Number,
    type: String,
    transport: String,
    date: String,
    duration: String,
  },
};
</script>
