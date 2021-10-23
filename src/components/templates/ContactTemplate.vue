<template>
  <form class="contact-template">
    <div class="blankets">
      <div class="input-data">
        <div>
          <label for="NomeCompleto"> Nome Completo </label>
          <input type="text" id="NomeCompleto" class="input-padrao" required />
        </div>

        <div>
          <label for="email">Email</label>
          <input
            type="email"
            id="email"
            class="input-padrao"
            required
            placeholder="seuemail@dominio.com"
          />
        </div>

        <div>
          <label for="telefone">Telefone</label>
          <input
            type="tel"
            id="telefone"
            class="input-padrao"
            required
            placeholder="(XX) XXXXX-XXXX"
          />
        </div>

        <div>
          <legend>Como prefere nosso contato?</legend>
          <div class="label">
            <label for="radio-email">
              <input
                type="radio"
                name="contato"
                value="email"
                id="radio-email"
              />
              Email
            </label>

            <label for="radio-telefone">
              <input
                type="radio"
                name="contato"
                value="telefone"
                id="radio-telefone"
              />
              Telefone
            </label>

            <label for="radio-wpp">
              <input
                type="radio"
                name="contato"
                value="wpp"
                id="radio-wpp"
                checked
              />
              WhatsApp
            </label>
          </div>
        </div>

        <div>
          <legend>Qual turno prefere atendimento?</legend>
          <div class="attendance">
            <select name="" id="">
              <option value="">Manhã</option>
              <option value="">Tarde</option>
              <option value="">Noite</option>
            </select>
          </div>
        </div>

        <label for="" class="checkbox" x>
          <input type="checkbox" checked />
          Gostaria de receber nossas novidades por e-mail?
        </label>
      </div>

      <div class="message">
        <label for="mensagem">Mensagem</label>
        <textarea
          name=""
          id="mensagem"
          cols="30"
          rows="10"
          class="input-padrao"
          required
        ></textarea>
      </div>
    </div>

    <input type="submit" value="Enviar Formulário" class="enviar" />
  </form>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<style scoped lang="scss">
.contact-template {
  text-align: center;
  grid-template-rows: auto 1fr;
  justify-items: center;
  display: grid;
  row-gap: 1em;
  padding: 1em;
  border-radius: 25px;
  box-shadow: 0.1rem 0.2rem 0.3rem 0.4rem rgba(68, 68, 160, 0.4);
  .blankets {
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-items: center;
    align-items: center;
    .message {
      display: grid;
      row-gap: 0.5em;
    }
    .input-data {
      display: grid;
      row-gap: 0.5rem;
      width: max-content;
      div {
        display: grid;
        grid-auto-flow: column;
      }
    }
  }
}
</style>
