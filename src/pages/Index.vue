<template>
  <q-page class="row items-center justify-evenly">
    <criteria-table-component
      title="Criteria table"
      active
      :criterias="criterias"
    ></criteria-table-component>
  </q-page>
</template>

<script lang="ts">
import { Criteria } from 'components/models';
import CriteriaTableComponent from 'components/CriteriaTableComponent.vue';
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'PageIndex',
  components: { CriteriaTableComponent },
  setup() {
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
    return { criterias };
  },
});
</script>
