<template>
  <div class="content">
    <header>
      <h1 class="volunteer-registration-part-two__title">
        CADASTRO VOLUNTÁRIO
      </h1>
      <router-link class="return__link" to="/volunteer-registration-part-one">
        <img
          src="../assets/img/return-icon.png"
          alt="Return Icon"
          class="return__icon"
        />
      </router-link>
    </header>
    <main>
      <img
        src="../assets/img/volunteer-registration-image.png"
        alt="Volunteer Registration Image"
        class="volunteer-registration__image"
      />
      <form class="volunteer-registration-part-two-form">
        <div class="form__cep-container">
          <label for="cep" class="cep__label">CEP:</label>
          <input
            type="text"
            class="cep__input"
            id="cep"
            v-mask="'#####-###'"
            v-model="formData.cep"
            @blur="fillAdrress"
            @keydown.enter="fillAdrress"
          />
        </div>
        <div class="form__road-container">
          <label for="road" class="road__label">Rua:</label>
          <input
            type="text"
            class="road__input"
            disabled
            v-model="formData.road"
          />
        </div>
        <div class="form__neighborhood-container">
          <label for="neighborhood" class="neighborhood__label">Bairro:</label>
          <input
            type="text"
            class="neighborhood__input"
            disabled
            v-model="formData.neighborhood"
          />
        </div>
        <div class="form__complement-container">
          <label for="complement" class="complement__label">Complemento:</label>
          <input
            type="text"
            class="complement__input"
            disabled
            v-model="formData.complement"
          />
        </div>
        <div class="form__state-container">
          <label for="state" class="state__label">Estado:</label>
          <input
            type="text"
            class="state__input"
            disabled
            v-model="formData.state"
          />
        </div>
        <div class="form__city-container">
          <label for="city" class="city__label">Cidade:</label>
          <input
            type="text"
            class="city__input"
            disabled
            v-model="formData.city"
          />
        </div>
        <router-link to="/volunteer-registration-part-one">
          <button type="button" class="volunteer-registration__button-return">
            Voltar
          </button>
        </router-link>
        <button
          type="button"
          @click="submitFormVolunteerPartTwo"
          class="volunteer-registration__button"
        >
          Continuar
        </button>
      </form>
    </main>
    <footer>
      <p class="footer__text">
        Copyright © 2023 | Todos os direitos reservados Green World
      </p>
    </footer>
  </div>
</template>

<script>
import fillAdrress from "../assets/js/methods/fill-address.js";
import submitFormVolunteerPartTwo from "../assets/js/methods/submit-form-volunteer-part-two.js";
import dataFormPartTwo from "../assets/js/data/data-form-part-two.js";

export default {
  name: "VolunteerRegistrationPartTwo",
  data() {
    const formData = this.$store.state.formData;
    const data = dataFormPartTwo(formData);
    return {
      ...data,
    };
  },
  methods: {
    fillAdrress,
    submitFormVolunteerPartTwo,
  },
};
</script>

<style scoped>
@import url("../assets/css/volunteerRegistrationPartTwo/generalStyle.css");
@import url("../assets/css/volunteerRegistrationPartTwo/limitsSizeStyle.css");
@import url("../assets/css/volunteerRegistrationPartTwo/volunteerRegistrationPartTwoStyle.css");
@import url("../assets/css/volunteerRegistrationPartTwo/volunteerRegistrationPartTwoResponsiveStyle.css");
@import url("../assets/css/volunteerRegistrationPartTwo/copyrightStyle.css");
@import url("../assets/css/volunteerRegistrationPartTwo/copyrightResponsiveStyle.css");
</style>
