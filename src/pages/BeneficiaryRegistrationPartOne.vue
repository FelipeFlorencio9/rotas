<template>
  <div class="content">
    <header>
      <h1 class="beneficiary-registration-part-one__title">
        CADASTRO BENEFICIADO
      </h1>
      <router-link class="return__link" to="/">
        <img
          src="../assets/img/return-icon.png"
          alt="Return Icon"
          class="return__icon"
        />
      </router-link>
    </header>
    <main>
      <img
        src="../assets/img/beneficiary-registration-image.png"
        alt="Beneficiary Registration Image"
        class="beneficiary-registration__image"
      />
      <form class="beneficiary-registration-part-one-form">
        <div class="form__photo-container">
          <input
            type="file"
            class="photo__label"
            id="photo"
            @change="uploadImage"
          />
          <label for="photo">
            <img
              src="../assets/img/photo-icon.png"
              alt="Photo Icon"
              class="photo__icon"
            />
          </label>
        </div>
        <div class="form__full-name-container">
          <label for="full-name" class="full-name__label">Nome completo:</label>
          <input
            type="text"
            class="full-name__input"
            id="fullName"
            maxlength="150"
            v-model="inputFullName"
          />
        </div>
        <div class="form__date-birth-container">
          <label for="date-birth" class="date-birth__label"
            >Data de nascimento:</label
          >
          <input
            type="text"
            class="date-birth__input"
            v-mask="'##/##/####'"
            v-model="inputDateBirth"
          />
        </div>
        <div class="form__rg-container">
          <label for="rg" class="rg__label">RG:</label>
          <input
            type="text"
            class="rg__input"
            v-mask="'##.###.###-#'"
            v-model="inputRg"
          />
        </div>
        <div class="form__cpf-container">
          <label for="cpf" class="cpf__label">CPF:</label>
          <input
            type="text"
            class="cpf__input"
            v-mask="'###.###.###-##'"
            v-model="inputCpf"
          />
        </div>
        <div class="form__phone-container">
          <label for="phone" class="phone__label">Telefone:</label>
          <input
            type="text"
            class="phone__input"
            v-mask="'(##) #####-####'"
            v-model="inputPhone"
          />
        </div>
        <div class="form__email-container">
          <label for="email" class="email__label">E-mail:</label>
          <input
            type="email"
            class="email__input"
            maxlength="256"
            v-model="inputEmail"
          />
        </div>
        <button
          type="button"
          @click="submitForm"
          class="beneficiary-registration__button"
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
import { getStorage, ref, uploadBytes, getDownloadURL } from "firebase/storage";
import { initializeApp } from "firebase/app";

const firebaseConfig = {
  apiKey: "AIzaSyDofRds_OjtPBMabg4-lS82cRWdLjXA4Zk",
  authDomain: "greenworld-f2763.firebaseapp.com",
  projectId: "greenworld-f2763",
  storageBucket: "greenworld-f2763.appspot.com",
  messagingSenderId: "549856611550",
  appId: "1:549856611550:web:ca75f1092264f9d607864f",
};

const app = initializeApp(firebaseConfig);
const storage = getStorage(app);

export default {
  name: "BeneficiaryRegistrationPartOne",
  data() {
    return {
      downloadURL: "",
      inputFullName: "",
      inputDateBirth: "",
      inputRg: "",
      inputCpf: "",
      inputPhone: "",
      inputEmail: "",
      formData: {
        photo: "",
        dateBirth: "",
        rg: "",
        cpf: "",
        phone: "",
        email: "",
      },
    };
  },
  methods: {
    async uploadImage(event) {
      this.formData.photo = this.downloadURL;

      const file = event.target.files[0];
      const storageRef = ref(storage, "images/" + file.name);

      await uploadBytes(storageRef, file);

      this.downloadURL = await getDownloadURL(storageRef);

      console.log("URL da imagem:", this.downloadURL);
    },
    submitForm() {
      this.formData.photo = this.downloadURL;
      this.formData.fullName = this.inputFullName;
      this.formData.dateBirth = this.inputDateBirth;
      this.formData.rg = this.inputRg;
      this.formData.cpf = this.inputCpf;
      this.formData.phone = this.inputPhone;
      this.formData.email = this.inputEmail;

      this.$store.commit("updateFormData", this.formData);
      console.log("formdata", this.formData);
      this.$router.push("/beneficiary-registration-part-two");
    },
  },
};
</script>
  
  <style scoped>
@import url("../assets/css/beneficiaryRegistrationPartOne/generalStyle.css");
@import url("../assets/css/beneficiaryRegistrationPartOne/limitsSizeStyle.css");
@import url("../assets/css/beneficiaryRegistrationPartOne/beneficiaryRegistrationPartOneStyle.css");
@import url("../assets/css/beneficiaryRegistrationPartOne/beneficiaryRegistrationPartOneResponsiveStyle.css");
@import url("../assets/css/beneficiaryRegistrationPartOne/copyrightStyle.css");
@import url("../assets/css/beneficiaryRegistrationPartOne/copyrightResponsiveStyle.css");
</style>
  