<template>
  <div id="app">
    <div class="header">
      <div class="navbar">
        <span class="logo" @click="current = 'Home'">DESAFIO-FÍSICA</span>
        <div class="nav-items">
          <span class="nav-item" @click="current = 'Content'">CONTEÚDO</span>
          <span class="nav-item" @click="current = 'Contact'">CONTATO</span>
        </div>
      </div>
      <img src="@/assets/imgs/banner.jpg" alt="" />
    </div>
    <main>
      <component :is="current" />
      <Footer />
    </main>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import {
  HomeTemplate,
  ContentTemplate,
  ContactTemplate,
} from '@/components/templates'
import { Footer } from '@/components/organisms'

export default defineComponent({
  name: 'App',
  components: {
    Home: HomeTemplate,
    Content: ContentTemplate,
    Contact: ContactTemplate,
    Footer,
  },

  data() {
    return {
      current: 'Home',
    }
  },
})
</script>

<style lang="scss">
#app {
  // background-color: rgba(176, 205, 235, 0.3);
  display: grid;
  justify-content: center;
  grid-template-rows: auto 1fr;
  font-family: Montserrat;
  .header {
    display: grid;
    justify-content: center;
    row-gap: 0.5rem;
    .navbar {
      padding: 0.5rem;
      display: grid;
      grid-auto-flow: column;
      justify-content: space-around;

      font-size: 1.1rem;
      font-size: bold;
      .logo {
        font-size: 1.4rem;

        transition: all 0.6s;
      }
      .logo:hover {
        background: rgb(33, 66, 99);
        color: white;
        cursor: pointer;
        transform: scale(1.05);
        padding: 0.12rem;
        border-radius: 10px;
      }
      .nav-items {
        display: grid;
        grid-auto-flow: column;

        column-gap: 1rem;
        .nav-item {
          transition: all 0.6s;
        }
        .nav-item:hover {
          background: rgb(33, 66, 99);
          color: white;
          cursor: pointer;
          transform: scale(1.05);
          padding: 0.12rem;
          border-radius: 10px;
        }
      }
    }
    img {
      max-width: 90vw;
      max-height: 25rem;
      box-shadow: 0.1rem 0.2rem 0.3rem 0.4rem rgba(68, 68, 160, 0.4);
      border-radius: 200px;
    }
  }
  main {
    max-width: 90%;
    align-self: center;
    margin: 1rem auto;
    display: grid;
    row-gap: 1em;
  }
}
</style>
