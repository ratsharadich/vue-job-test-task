<!-- Список экскурсий -->
<template>
  <section class="excursion-list d-flex flex-column">
    <Tile
      class="excursion-list__tile"
      v-for="excursion of listMock"
      :key="excursion.id"
      :name="excursion.name"
      :info="Object.values(excludeNameAndId(excursion)).filter(Boolean)"
    />
  </section>
</template>

<script>
import Tile from './components/Tile.vue';

export default {
  name: 'ExurcionsList',
  data() {
    return {
      listMock: [
        {
          id: 1,
          name: '«Город сыра и мира»',
          rating: {
            value: 5,
            iconName: 'mdi-star-outline',
          },
          type: {
            value: 'Историческая',
          },
          transport: {
            value: 'На автобусе',
            iconName: 'mdi-bus',
          },
          date: {
            value: '28 марта',
          },
          duration: {
            value: '9 часов',
            iconName: 'mdi-clock-time-three-outline',
          },
          limit: {
            value: 'до 20',
            iconName: 'mdi-account',
          },
        },
        {
          id: 2,
          name: 'Экскурсия в национальный парк "Куршская коса"',
          rating: {
            value: 5,
            iconName: 'mdi-star-outline',
          },
          type: {
            value: 'Обзорная',
          },
          transport: {
            value: 'На автобусе',
            iconName: 'mdi-bus',
          },
          date: {
            value: '25 марта',
          },
          duration: {
            value: '6 часов',
            iconName: 'mdi-clock-time-three-outline',
          },
          limit: {
            value: 'до 25',
            iconName: 'mdi-account',
          },
        },
        {
          id: 3,
          name: '«О кирках, рыцарях и замках»',
          rating: {
            value: 5,
            iconName: 'mdi-star-outline',
          },
          type: {
            value: 'Историческая',
          },
          transport: {
            value: 'На автобусе',
            iconName: 'mdi-bus',
          },
          date: {
            value: '29 марта',
          },
          duration: {
            value: '6 часов',
            iconName: 'mdi-clock-time-three-outline',
          },
          limit: {
            value: 'до 40',
            iconName: 'mdi-account',
          },
        },
        {
          id: 4,
          name: 'Экскурсия в Янтарный',
          rating: null,
          type: {
            value: 'Историческая',
          },
          transport: {
            value: 'На автобусе',
            iconName: 'mdi-bus',
          },
          date: {
            value: '29 марта',
          },
          duration: {
            value: '6 часов',
            iconName: 'mdi-clock-time-three-outline',
          },
          limit: {
            value: 'до 10',
            iconName: 'mdi-account',
          },
        },
      ],
    };
  },
  methods: {
    excludeNameAndId(excursion) {
      const {name, id, ...rest} = excursion;
      return rest;
    },
  },
  components: {
    Tile,
  },
};
</script>
