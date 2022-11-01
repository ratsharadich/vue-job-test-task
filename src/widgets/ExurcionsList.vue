<template>
  <section class="excursion-list">
    <ExcursionTile
      v-for="excursion of listMock"
      :key="excursion.id"
      :name="excursion.name"
      :rating="excursion.rating"
      :type="excursion.type"
      :transport="excursion.transport"
      :date="excursion.date"
      :duration="excursion.duration"
    />
  </section>
</template>

<script>
import './styles.css';
import ExcursionTile from './components/ExurcionTile.vue';

export default {
  name: 'ExurcionsList',
  data() {
    return {
      listMock: [
        {
          id: 1,
          name: '«Город сыра и мира»',
          rating: 5,
          type: 'Историческая',
          transport: 'На автобусе',
          date: '28 марта',
          duration: '9 часов',
        },
        {
          id: 2,
          name: 'Экскурсия в национальный парк "Куршская коса"',
          rating: 5,
          type: 'Обзорная',
          transport: 'На автобусе',
          date: '25 марта',
          duration: '6 часов',
        },
        {
          id: 3,
          name: '«О кирках, рыцарях и замках»',
          rating: 5,
          type: 'Историческая',
          transport: 'На автобусе',
          date: '29 марта',
          duration: '6 часов',
        },
        {
          id: 4,
          name: 'Экскурсия в Янтарный',
          rating: null,
          type: 'Историческая',
          transport: 'На автобусе',
          date: '29 марта',
          duration: '6 часов',
        },
      ],
    };
  },
  components: {
    ExcursionTile,
  },
};
</script>
