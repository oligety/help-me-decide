<script setup lang="ts">
import { defineProps, PropType } from 'vue';
import { Criteria } from './models';

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  criterias: {
    type: Array as PropType<Criteria[]>,
    default: () => [],
  },
});
</script>

<template>
  <div class="q-pa-md">
    <div v-for="criteria in props.criterias" :key="criteria.id" class="row">
      <div class="col">{{ criteria.id }}</div>
      <div class="col">{{ criteria.name }}</div>
    </div>
  </div>
</template>
