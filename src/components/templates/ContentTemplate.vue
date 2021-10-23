<template>
  <div class="contents-template">
    <div class="content">
      <h2>Mecânica</h2>
      <img src="@/assets/imgs/mecanica.png" />
      <p class="descricao">Leis de Newton</p>
    </div>
    <div class="content">
      <h2>Termodinâmica</h2>
      <img src="@/assets/imgs/termodinamica.png" />
      <p class="descricao">Transformações físicas</p>
    </div>
    <div class="content">
      <h2>Ondulatória</h2>
      <img src="@/assets/imgs/ondulatoria.png" />
      <p class="descricao">Oscilações e ondas</p>
    </div>
    <div class="content">
      <h2>Eletromagnetismo</h2>
      <img src="@/assets/imgs/eletromagnetismo.png" />
      <p class="descricao">Campos e radiações eletromagnéticas.</p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<style scoped lang="scss">
.contents-template {
  margin: 1rem auto;
  display: grid;
  grid-template-columns: repeat(4, 20%);
  column-gap: 1rem;
  justify-content: space-evenly;
  text-align: center;
  .content {
    cursor: pointer;
    border-radius: 25px;
    box-shadow: 0.1rem 0.2rem 0.3rem 0.4rem rgba(68, 68, 160, 0.4);
    display: grid;
    row-gap: 1rem;
    align-content: center;
    justify-content: center;
    img {
      max-width: 100%;
    }
  }
}
</style>
