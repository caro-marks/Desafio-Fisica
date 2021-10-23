<template>
  <div class="home-template">
    <h2 class="titulo-principal">Sobre o Desafio - Física</h2>

    <div class="main">
      <img class="utensilios" src="@/assets/imgs/estudos.jpeg" alt="livros" />

      <div class="first">
        <p>
          Fundada para democratizar o acesso a universidade, o
          <strong>Projeto Desafio</strong> traz para o público estudantil de
          diferentes classes o esforço coletivo de universitários em oferecer
          aulas com os conteúdos programáticos das áreas cobradas nos
          vestibulares. Nesse contexto, o grupo de alunos responsáveis pela área
          da Física reune aulas e artigos com os temas tratados durante o ano
          letivo neste website.
        </p>

        <div class="second">
          <p id="conteudo">
            <em
              >Nossos conteúdos principais são dividos em:
              <strong
                >"Mecânica", "Termodinâmica, "Ondulatória", e "Eletromagnetismo"
              </strong>
              .
            </em>
          </p>

          <p>
            Os professores são da área da licenciatura, e procuram apresentar os
            conceitos mais relevantes, se dedicando para esclarecer dúvidas e
            auxiliar na resolução de exercícios.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({})
</script>

<style scoped lang="scss">
strong {
  font-weight: bold;
}
.home-template {
  margin: 1rem auto;
  text-align: center;
  display: grid;
  row-gap: 0.5rem;
  .titulo-principal {
    font-size: 1rem;

    padding: 0.2rem;
    font-weight: bolder;
  }
  .main {
    display: grid;
    grid-template-columns: 20% auto;
    column-gap: 1rem;
    align-items: center;
    box-shadow: 0.1rem 0.2rem 0.3rem 0.4rem rgba(68, 68, 160, 0.4);
    border-radius: 50px;
    img {
      max-width: 90%;
      min-width: 90px;
      border-radius: 50px 0 0 50px;
    }
    .first {
      display: grid;
      row-gap: 1.5rem;
      p {
      }
    }
    .second {
      display: grid;
      grid-template-columns: 40% 1fr;
      column-gap: 1em;
      p {
      }
      em strong {
        color: rgb(27, 27, 102);
      }
    }
  }
}
</style>
