<script setup lang="ts">
import { ref } from 'vue';
import { Criteria } from 'components/models';
import CriteriaListComponent from 'components/CriteriaListComponent.vue';

// variables
const criterias = ref<Criteria[]>([
  {
    id: 1,
    name: 'Criteria 1',
  },
  {
    id: 2,
    name: 'Criteria 2',
  },
  {
    id: 3,
    name: 'Criteria 3',
  },
  {
    id: 4,
    name: 'Criteria 4',
  },
  {
    id: 5,
    name: 'Criteria 5',
  },
]);

// functions
function addCriteria() {
  console.info('test');
  return true;
}
</script>

<template>
  <q-page>
    <!-- Add criteria -->
    <q-btn color="primary" label="Add criteria" @click="addCriteria" />

    <!-- Criteria list -->
    <CriteriaListComponent
      title="Criteria table"
      active
      :criterias="criterias"
    ></CriteriaListComponent>
  </q-page>
</template>
