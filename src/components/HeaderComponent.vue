<template>
  <header class="container-row">
    <!-- LOGO -->
    <div class="container logo">
      <img src="@/assets/logo.png" alt="Vue.js" />
    </div>

    <div class="container-row bar">
      <!-- COMPANY NAME -->
      <address class="container company-name">
        <span>surreal são paulo</span>
        <span>vtex</span>
      </address>

      <!-- NOTIFICATION -->
      <div class="container notification">
        <span class="material-icons">notifications_active</span>
      </div>
    </div>

    <!-- USER -->
    <div class="container-row users">
      <span>Olá, Ricardo</span>
      <span class="material-icons">account_circle</span>
    </div>
  </header>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    name: 'HeaderComponent',
    data() {
      return {
        isOpenDrawer: false,
      };
    },
    methods: {
      toggleDrawer() {
        this.isOpenDrawer = !this.isOpenDrawer;
      },
    },
  });
</script>

<style lang="scss">
  header {
    width: 100%;
    height: 70px;
    background-color: var(--primary);

    .logo {
      width: 60px;
      height: 60px;

      img {
        width: 70%;
        object-fit: contain;
      }
    }

    .bar {
      width: calc(100% - 60px);
      padding: 8px;

      address {
        margin-left: 16px;
        align-items: flex-start;
        padding: 4px 8px;
        border-radius: 8px;
        border: solid 1px var(--light);

        span {
          opacity: 0.8;
          color: var(--light);
          font-size: 0.8rem;
          font-weight: 600;
        }
        span:first-child {
          text-transform: capitalize;
        }
        span:last-child {
          text-transform: uppercase;
        }
      }
    }

    .notification {
      width: 60px;
      height: 60px;

      .material-icons {
        color: var(--light);
      }
    }

    .users {
      padding: 8px;
      border-left: solid 1px var(--light);

      span {
        opacity: 0.8;
        color: var(--light);
        font-size: 0.8rem;
        font-weight: 600;
      }

      .material-icons {
        margin-left: 8px;
        font-size: 2.5rem;
        color: var(--grey);
      }

      @media (max-width: 768px) {
        span:first-child {
          display: none;
        }
      }
    }
  }
</style>