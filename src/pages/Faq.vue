<template>
  <header>
    <h1 class="privacy-policy__title">Perguntas Frequentes</h1>
    <router-link class="return__link" to="/">
      <img
        src="../assets/img/return-icon.png"
        alt="Return Icon"
        class="return__icon"
      />
    </router-link>
  </header>
  <main>
    <div class="privacy-policy__content-text">
      <p class="privacy-policy-description__text">
        Separamos algumas das perguntas que mais recebemos com o objetivo de
        sanar dúvidas à respeito dos nossos projetos. Ainda assim, se
        necessário, não hesite em entrar em contato conosco. Estamos à sua
        disposição!
      </p>
      <img
        class="privacy-policy__content-text__image"
        src="../assets/img/privacy-policy.png"
        alt=""
      />
    </div>
    <ul class="privacy-policy-container">
      <li
        @click="
          changeState(
            '.information-we-collect',
            '.information-we-collect__plus-sign'
          )
        "
        class="privacy-policy"
      >
        <div class="privacy-policy__button">
          <h2 class="privacy-policy__question">
            Preciso morar em Alagoas para ser um voluntário?
          </h2>
          <img
            class="information-we-collect__plus-sign plus-sign__icon"
            src="../assets/img/plus-sign-icon.png"
            alt="Plus sign"
          />
        </div>
        <div class="information-we-collect privacy-policy__content-info">
          <p class="privacy-policy__text">
            1.1 Informações fornecidas por você: Quando você utiliza o nosso
            site, podemos solicitar informações pessoais, como nome, endereço de
            e-mail, informações de contato e outras informações relevantes para
            o uso dos nossos serviços.
          </p>
          <p class="privacy-policy__text">
            1.2 Informações de uso: Coletamos informações sobre como você
            utiliza o nosso site, como endereço IP, tipo de navegador, páginas
            visitadas, duração da visita e outros dados de uso do site.
          </p>
        </div>
      </li>
      <li
        @click="
          changeState('.use-of-information', '.use-of-information__plus-sign')
        "
        class="privacy-policy"
      >
        <div class="privacy-policy__button">
          <h2 class="privacy-policy__question">
            Quais requisitos preciso atender para ser um beneficiado?
          </h2>
          <img
            class="use-of-information__plus-sign plus-sign__icon"
            src="../assets/img/plus-sign-icon.png"
            alt="Plus sign"
          />
        </div>
        <div class="use-of-information privacy-policy__content-info">
          <p class="privacy-policy__text">
            2.1 Utilização interna: Utilizamos as informações coletadas para
            fornecer e melhorar os nossos serviços, personalizar a sua
            experiência no site, responder a consultas, enviar informações sobre
            os nossos produtos ou serviços, e para outros fins internos
            relacionados ao funcionamento do site.
          </p>
          <p class="privacy-policy__text">
            2.2 Comunicação: Podemos utilizar o seu endereço de e-mail para
            enviar comunicações relacionadas aos nossos serviços, como
            atualizações, boletins informativos ou promoções. Você pode optar
            por não receber tais comunicações a qualquer momento, seguindo as
            instruções de bloqueio de inscrição fornecidas.
          </p>
        </div>
      </li>
      <li
        @click="
          changeState('.information-sharing', '.information-sharing__plus-sign')
        "
        class="privacy-policy"
      >
        <div class="privacy-policy__button">
          <h2 class="privacy-policy__question">
            Como solicito a ajuda novamente?
          </h2>
          <img
            class="information-sharing__plus-sign plus-sign__icon"
            src="../assets/img/plus-sign-icon.png"
            alt="Plus sign"
          />
        </div>
        <div class="information-sharing privacy-policy__content-info">
          <p class="privacy-policy__text">
            3.1 Terceiros: Podemos compartilhar suas informações pessoais com
            terceiros somente quando necessário para fornecer os serviços por
            você ou quando exigido por lei. Esses terceiros são obrigados a
            proteger a privacidade e a segurança das suas informações pessoais.
          </p>
          <p class="privacy-policy__text">
            3.2 Parceiros e produtores de serviços: Podemos compartilhar
            informações com parceiros e líderes de serviços que nos auxiliam na
            operação do site e na prestação de nossos serviços. Esses parceiros
            e fluxos de serviços estão sujeitos a obrigações contratuais de
            confidencialidade e podem utilizar as informações apenas para os
            fins acordados.
          </p>
        </div>
      </li>
      <li
        @click="
          changeState(
            '.information-security',
            '.information-security__plus-sign'
          )
        "
        class="privacy-policy"
      >
        <div class="privacy-policy__button">
          <h2 class="privacy-policy__question">
            O projeto contempla qual região?
          </h2>
          <img
            class="information-security__plus-sign plus-sign__icon"
            src="../assets/img/plus-sign-icon.png"
            alt="Plus sign"
          />
        </div>
        <div class="information-security privacy-policy__content-info">
          <p class="privacy-policy__text">
            4.1 Medidas de segurança: Implementamos medidas de segurança para
            proteger suas informações pessoais contra acesso não autorizado, uso
            indevido, divulgação ou alteração. No entanto, nenhuma transmissão
            de dados pela Internet ou método de armazenamento eletrônico é
            completamente segura, e não podemos garantir a segurança absoluta
            das informações.
          </p>
        </div>
      </li>
      <li
        @click="
          changeState(
            '.links-to-other-sites',
            '.links-to-other-sites__plus-sign'
          )
        "
        class="privacy-policy"
      >
        <div class="privacy-policy__button">
          <h2 class="privacy-policy__question">
            A partir de qual idade posso me tornar um voluntário?
          </h2>
          <img
            class="links-to-other-sites__plus-sign plus-sign__icon"
            src="../assets/img/plus-sign-icon.png"
            alt="Plus sign"
          />
        </div>
        <div class="links-to-other-sites privacy-policy__content-info">
          <p class="privacy-policy__text">
            5.1 Links externos: O nosso site pode conter links para outros sites
            de terceiros. Esta Política de Privacidade se aplica apenas ao nosso
            site, e não nos responsabilizamos pelas práticas de privacidade
            desses sites externos.
          </p>
        </div>
      </li>
    </ul>
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
          <a href="#" class="social__footer"
            ><i class="fab fa-instagram"></i
          ></a>
        </li>
        <li>
          <a href="#" class="social__footer"
            ><i class="fab fa-facebook-f"></i
          ></a>
        </li>
      </ul>
    </nav>
    <div class="support-content">
      <span class="support__title">Suporte</span>
      <div class="support__links">
        <a class="support__link" href="./faq.html">FAQ</a>
        <a class="support__link" href="#">Política de privacidade</a>
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
import plusSign from '@/assets/img/plus-sign-icon.png'
import minusSign from '@/assets/img/minus-sign-icon.png'

export default {
  name: "PrivacyPolicy",
  methods: {
    changeState(element, image) {
      let display = document.querySelector(element).style.display;
      let img = document.querySelector(image);

      if (display == "block") {
        document.querySelector(element).style.display = "none";
        img.src = plusSign;
      } else {
        document.querySelector(element).style.display = "block";
        img.src = minusSign;
      }
    },
  },
};
</script>
      
<style scoped>
@import url("../assets/css/faq/generalStyle.css");
@import url("../assets/css/faq/faqStyle.css");
@import url("../assets/css/faq/faqResponsiveStyle.css");
</style>
      