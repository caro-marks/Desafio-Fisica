<template>
  <div class="contato">
    <p>&copy; Desenvolvido por Marcos Alexandre</p>
    <a href="https://www.linkedin.com/in/caro-marks/"> Linkedin </a>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<style scoped lang="scss">
.contato {
  display: flex;
  justify-content: center;
  a {
    text-decoration: none;
    margin-left: 0.5em;
  }
}
</style>
