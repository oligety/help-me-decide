<template>
  <div>
    <p>{{ title }}</p>
    <ul>
      <li v-for="criteria in criterias" :key="criteria.id">
        {{ criteria.id }} - {{ criteria.name }}
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import { Criteria } from './models';

export default defineComponent({
  name: 'CriteriaTableComponent',
  props: {
    title: {
      type: String,
      required: true,
    },
    criterias: {
      type: Array as PropType<Criteria[]>,
      default: () => [],
    },
  },
  setup() {
    return {};
  },
});
</script>
