<template>
  <div class="app">
    <HeaderComponent />
    <section id="body" class="container-row">
      <AsideComponent />
      <router-view/>
    </section>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HeaderComponent from './components/HeaderComponent.vue';
import AsideComponent from './components/AsideComponent.vue';

export default defineComponent({
  name: 'App',
  components: {
    HeaderComponent,
    AsideComponent,
  },
});
</script>

<style lang="scss">
  :root {
    --background: ##E5E5E5;
    --primary: #9206E9;
    --dark: #1e293b;
    --grey: #F6F6F6;
    --light: #f1f5f9;
    --sidebar-width: 250px;
  }
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Fira Sans', sans-serif;
  }
  body {
    background: var(--background);
  }
  button {
    cursor: pointer;
    appearance: none;
    border: none;
    outline: none;
    background: none;
  }
  .app {
    display: flex;
    flex-direction: column;
    main {
      flex: 1 1 0;
      padding: 2rem;

      @media (min-width: 768px) {
        padding: 6rem;
      }
    }
  }
  #body {
    align-items: flex-start;
    justify-content: flex-start;
  }
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .container-row {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
  .container-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 1rem;
  }
</style>