<template>
  <div class="dashboard">
    <h1>Dashboard</h1>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    name: 'DashboardView',
  });
</script>

<style lang="scss" scoped>
  .dashboard {
    padding: 1rem;
    width: calc(100% - (2rem + 32px));
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-left: 4rem;

    @media (min-width: 768px) {
      width: calc(100% - (2rem + 64px));
      margin-left: 0rem;
    }
  }
</style>