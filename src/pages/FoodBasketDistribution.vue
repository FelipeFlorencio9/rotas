<template>
  <header>
    <div class="food_basket_distribution_project-container">
      <h1 class="food-basket-distribution-project__title">
        DISTRIBUIÇÃO DE CESTAS BÁSICAS
      </h1>
      <router-link class="return__link" to="/"><img src="../assets/img/return-icon.png" alt="Return Icon"
          class="return__icon" /></router-link>
    </div>
  </header>
  <main>
    <div class="project-goal limit">
      <h2 class="project-goal__title">Objetivo do projeto</h2>
      <p class="project-goal__text">
        Em meio aos desafios enfrentados pelas comunidades carentes, onde a escassez de recursos básicos é uma realidade
        diária, a distribuição de cestas básicas tem se destacado como uma forma eficiente e solidária de atender às
        necessidades imediatas de alimentação. Essas iniciativas têm como objetivo principal levar esperança e alimentos
        para as famílias mais aptas, garantindo que elas tenham acesso a uma alimentação adequada e digna.
      </p>
    </div>
    <div class="how-is-possible limit">
      <h2 class="how-is-possible__title">Como é possível?</h2>
      <p class="project-goal__text">
        A arrecadação de recursos é uma etapa crucial para o sucesso do projeto. Por meio de parcerias com empresas
        locais, são promovidas campanhas de doação de alimentos. Além disso, são organizados eventos solidários, como
        bazares e festas beneficentes, com o objetivo de arrecadar fundos para a compra das cestas básicas, e é claro a
        ajuda de nossos patrocinadores.
      </p>
    </div>
    <div class="project-images-container">
      <div class="project-images">
        <img src="../assets/img/food_basket_distribution_project-image.png" alt="Project Image" class="project-image" />
        <img src="../assets/img/food_basket_distribution_project-image.png" alt="Project Image" class="project-image" />
        <img src="../assets/img/food_basket_distribution_project-image.png" alt="Project Image" class="project-image" />
      </div>
    </div>
  </main>
  <footer>
    <div class="meaning-of-agriculture-content">
      <span class="meaning-of-agriculture__title">Agricultura</span>
      <p class="meaning-of-agriculture__text">
        A agricultura é uma prática econômica que consiste no uso dos solos para
        cultivo de vegetais a fim de garantir a subsistência alimentar do ser
        humano.
      </p>
    </div>
    <nav class="social-media-container">
      <ul class="social-media__footer">
        <li>
          <a href="#" class="social__footer"><i class="fab fa-twitter"></i></a>
        </li>
        <li>
          <a href="#" class="social__footer"><i class="fab fa-instagram"></i></a>
        </li>
        <li>
          <a href="#" class="social__footer"><i class="fab fa-facebook-f"></i></a>
        </li>
      </ul>
    </nav>
    <div class="support-content">
      <span class="support__title">Suporte</span>
      <div class="support__links">
        <router-link class="support__link" to="/faq"> FAQ </router-link>
        <router-link class="support__link" to="/privacy-policy">
          Política de privacidade
        </router-link>
      </div>
    </div>
    <div class="contact-content">
      <span class="contact__title">Contate-nos</span>
      <ul class="contacts">
        <li class="contact">greenworld@gmail.com</li>
        <li class="contact">(11) 4774-4700</li>
        <li class="contact">Alagoas</li>
      </ul>
    </div>
    <p class="copyright">
      Copyright © 2023 | Todos os direitos reservados Green World
    </p>
  </footer>
</template>

<script>
export default {
  name: "FoodBasketDistribution",
};
</script>

<style scoped>
@import url("../assets/css/generalStyle.css");
@import url("../assets/css/foodBasketDistribution/limitsSizeStyle.css");
@import url("../assets/css/foodBasketDistribution/foodBasketDistributionStyle.css");
@import url("../assets/css/foodBasketDistribution/foodBasketDistributionResponsiveStyle.css");
@import url("../assets/css/footer/footerResponsiveStyle.css");
@import url("../assets/css/footer/footerStyle.css");
</style>
