<template>
  <div class="search">
    <!-- ADD ADDRESS -->
    <div class="container add-address">
      <form class="container">
        <input type="search" name="search" id="search" />
        <button type="submit">
          <span class="material-icons">add</span>
          <span>Adicionar endereço</span>
        </button>
      </form>
      
      <div class="container-row list-zip-code">
        <span class="container">
          <span class="material-icons icon">where_to_vote</span>
        </span>
        <span class="container zip-code">cep</span>
        <span class="container" style="color:gray">659165-568</span>
      </div>

      <div class="container address-generator">
        <button>
          <span>Gerar endereços</span>
        </button>
      </div>
    </div>

    <hr />

    <!-- ADDRESS LIST -->
    <div class="container box-list">
      <div class="container-row address-list">
        <span class="container icons">
          <span class="material-icons">where_to_vote</span>
        </span>

        <!-- CONTAINER ADDRESS -->
        <address class="container-row">
          <div class="container address">
            <span>Rua Mandaguari, nº 556</span>
            <span>Imperatriz-MA</span>
          </div>
          <span class="zip-code">65913-565</span>
        </address>

        <button class="container icons">
          <span class="material-icons delete">delete</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    name: 'SearchView',
  });
</script>

<style lang="scss" scoped>
  .search {
    max-width: 600px;
    padding: 1rem;
    width: calc(100% - (2rem + 32px));
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-left: 4rem;

    .add-address {
      width: 100%;

      form {
        width: 100%;
        
        input {
          width: 100%;
          height: 50px;
          padding: 0.5rem;
          border-radius: 0.5rem;
        }

        button {
          margin: 1rem 0;
        }

        @media (min-width: 768px) {
          flex-direction: row;
          justify-content: space-between;

          input {
            width: calc(50% - 0.5rem);
          }
          button {
            width: calc(50% - 0.5rem);
          }
        }
      }

      .list-zip-code {
        width: 100%;
        justify-content: flex-start;
        margin-bottom: 1rem;

        .icon {
          color: var(--primary);
        }
        .zip-code {
          margin-right: 4px;
          text-transform: uppercase;
          font-weight: bold;
          color: var(--dark);
        }
      }

      button {
        display: flex;
        width: 100%;
        height: 52px;
        align-items: center;
        justify-content: center;
        flex-direction: row;
        background-color: var(--primary);
        padding: 0.5rem;
        border-radius: 0.5rem;
        
        &:hover {
          opacity: 0.8;
          transition: 0.3s;
        }

        span {
          color: var(--light);
          font-weight: bold;
        }
      }

      .address-generator {
        width: 100%;
        align-items: flex-end;
      }

      @media (min-width: 768px) {
        button {
          width: calc(50% - 0.5rem);
        }
      }
    }

    hr {
      margin: 1.5rem 0;
      border: 0;
      border-top: 1px solid #ccc;
      width: 100%;
    }
    .box-list {
      width: 100%;

      .address-list {
        width: 100%;
        box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.5);
        border-radius: 8px;
        padding: 1rem;
        margin-bottom: 1rem;

        .icons {
          .material-icons {
            color: var(--primary);
          }
          .delete {
            color: red;
            opacity: 0.8;
            margin-left: 8px;
          }
        }
        button {
          transition: 0.3s;
          background: none;
          border: none;
          padding: 0;
          margin: 0;

          &:hover {
            cursor: pointer;
            opacity: 0.5;
          }
        }
        address {
          width: 100%;
          padding: 0px 1rem;
          border-right: solid 1px #ccc;

          .address {
            align-items: flex-start;
            font-weight: 600;
          }
          
          @media (max-width: 768px) {
            align-items: flex-start;
            flex-direction: column;

            .zip-code {
              margin-top: 1rem;
            }
          }
        }
      }
    }

    @media (min-width: 768px) {
      width: calc(100% - (2rem + 64px));
      margin-left: 0rem;
    }
  }
</style>