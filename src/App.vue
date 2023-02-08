<template>
  <Header></Header>
  <main class="wrapper">
    <section id="home">
      <div class="welcome">
        <div class="welcome-text">
          <h1>Saúde em <span>primeiro lugar</span> 🍇.</h1>
          <p>
            A nutrição é extremamente importante para levar uma vida saudável.
            Com uma alimentação calculada, você pode atingir seus objetivos com
            relação ao seu corpo (seja você carnívoro, vegetariano ou vegano), e
            eu estou aqui para guiar você nessa jornada!
          </p>
        </div>
        <a href="https://wa.me/5551999004881" target="_blank"><button>Vamos começar!</button></a>
        <img class="bfr bfr-1" src="./assets/ellipse-1.svg" />
        <img class="bfr bfr-2" src="./assets/ellipse-2.svg" />
      </div>
    </section>
    <section id="goals">
      <h2>Qual é o seu <span>objetivo</span>?</h2>
      <div class="cards">
        <GoalCard @click="isMuscleGainModal = true" :image="require('@/assets/ganho-massa.png')" title="Ganho de massa"
          content="Alimentação calculada para o aumento de massa magra, de maneira saudável e eficaz."></GoalCard>
        <GoalCard @click="isWeightLossModal = true" :image="require('@/assets/perda-de-peso.png')" title="Perda de peso"
          content="Dietas planejadas visando a reeducação alimentar, que traz benefícios a curto e longo prazo para pessoas acima do peso.">
        </GoalCard>
        <GoalCard @click="isLongevityModal = true" :image="require('@/assets/longevidade.png')" title="Longevidade"
          content="Alimentação planejada visando a qualidade de vida e até mesmo sensação de rejuvenecimento.">
        </GoalCard>
      </div>
      <div class="footer">
        <p>
          Busca algo mais <span>específico</span>? Vamos olhar as
          especializações.
        </p>
        <a href="#specializations"><font-awesome-icon icon="fa-solid fa-angles-down" class="fa-xl"
            style="color: var(--brand-purple)" /></a>
      </div>
      <img class="bfr bfr-3" src="./assets/ellipse-3.svg" />
    </section>
    <section id="specializations">
      <h2>Especializações</h2>
      <div class="cards">
        <SpecializationCard title="Nutrição vegetariana 🥑"
          content="A alimentação vegetariana é extremamente saudável, se praticada da maneira correta. Com alimentos balanceados, você pode aderir de forma totalmente saudável a uma vida vegetariana 💚."
          :image="require('@/assets/vegetariano.png')"></SpecializationCard>
        <SpecializationCard title="Comportamento alimentar  🍔"
          content="Alguns alimentos podem ser vistos como “vilões” de uma vida saudável. Mas na verdade, tudo é uma questão de hábito, e com uma reeducação alimentar você pode ter uma alimentação sadável e, ao mesmo tempo, curtir a vida 🥂."
          :image="require('@/assets/comportamento-alimentar.png')"></SpecializationCard>
        <SpecializationCard title="Nutrição na cirurgia bariátrica 🩺"
          content="A cirurgia bariátrica é extremamente agressiva para o nosso corpo (e falo por experiência própria). Então, balancear as refeições depois de passar por esse procedimento é essencial para manter uma alimentação segura e nutritiva."
          :image="require('@/assets/cirurgia-bariatrica.png')"></SpecializationCard>
      </div>
      <img src="./assets/ellipse-4.svg" class="bfr bfr-4" />
    </section>
    <section id="about">
      <div class="content">
        <div class="text">
          <h2>Prazer, eu sou a <span>Juu</span>.</h2>
          <div class="bio">
            <p>
              Meu nome é <span>Juliane Marrone</span> e, como alguém apaixonada
              pela área da nutrição, estou aqui para ajudar você a atingir seus
              objetivos com relação ao seu corpo e saúde!
            </p>
            <p>
              Quando estudamos nutrição, aprendemos que o bolinho ou aquele
              chocolatinho depois do almoço não são vilões da balança (claro, se
              ingeridos com moderação 😅).
            </p>
            <p>
              Minha missão aqui é ajudar as pessoas a se tornarem mais
              <span>saudáveis</span> de acordo com seus objetivos, tudo de
              maneira descomplicada e amigável.
            </p>
          </div>
        </div>
        <img src="./assets/mana-eric.jpg" alt="" />
      </div>
    </section>
    <section id="contact">
      <div class="content">
        <img src="./assets/veggie-meal.png" alt="Refeição vegetariana" />
        <div class="text">
          <h2>Entre em contato comigo</h2>
          <p>
            Quer melhorar a sua qualidade de vida ou tirar alguma dúvida? Você
            pode entrar em contato comigo pelo WhatsApp, rápido e prático!
          </p>
          <a href="https://wa.me/5551999004881" target="_blank"><button>
              <font-awesome-icon class="fa-2xl" icon="fa-brands fa-whatsapp" />
              Agende sua consulta
            </button></a>
        </div>
      </div>
    </section>
  </main>
  <div v-if="isWeightLossModal == true">
    <WeightLossModal @closeWeightModal="closeWeightModal"></WeightLossModal>
  </div>
  <div v-if="isMuscleGainModal == true">
    <MuscleGainModal @closeMuscleModal="closeMuscleModal"></MuscleGainModal>
  </div>
  <div v-if="isLongevityModal == true">
    <LongevityModal @closeLongevityModal="closeLongevityModal"></LongevityModal>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import GoalCard from "./components/GoalCard.vue";
import SpecializationCard from "./components/SpecializationCard.vue";
import WeightLossModal from "./components/WeightLossModal.vue";
import MuscleGainModal from "./components/MuscleGainModal.vue";
import LongevityModal from "./components/LongevityModal.vue"


export default {
  name: "App",

  data() {
    return {
      isMuscleGainModal: false,
      isWeightLossModal: false,
      isLongevityModal: false,
    };
  },

  components: {
    Header,
    GoalCard,
    SpecializationCard,
    WeightLossModal,
    MuscleGainModal,
    LongevityModal
  },

  methods: {
    closeMuscleModal() {
      this.isMuscleGainModal = false;
    },
    closeWeightModal() {
      console.log("teste")
      this.isWeightLossModal = false;
    },
    closeLongevityModal() {
      this.isLongevityModal = false;
    },
  },
};
</script>

<style>
:root {
  --brand-purple: #9e00ff;
  --brand-purple-shadow: #ca75ff;
  --brand-purple-shadow-light: #e3b6ff;
  --brand-purple-shadow-lighter: #f2dcff;
  --title: #151515;
  --paragraph: #4d4d4d;
}

html {
  scroll-behavior: smooth;
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.bfr {
  position: absolute;
  z-index: -10;
}

.bfr-1 {
  right: 0;
  top: 0;
  width: 43%;
}

.bfr-2 {
  left: 0;
  top: 35%;
  width: 24%;
  opacity: 0.8;
}

.bfr-3 {
  right: 0;
  margin-top: 25rem;
  width: 18%;
}

.bfr-4 {
  left: -30%;
  width: 100%;
  height: 90rem;
  top: 180%;
}

@media only screen and (min-width: 992px) {
  section {
    height: calc(100vh + 5rem);
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    /* padding: 4rem; */
    padding-top: 8rem;
  }

  section h2 {
    font-size: 2rem;
    text-align: center;
  }

  #home {
    height: calc(100vh - 6rem);
    justify-content: center;
    padding: 0;
  }

  .wrapper {
    max-width: 70rem;
    margin: 0 auto;
  }

  span {
    color: var(--brand-purple);
  }

  body,
  button,
  textarea,
  input {
    font-family: "Poppins", sans-serif;
    font-size: 1.125rem;
  }

  h1,
  h2,
  h3,
  h4 {
    color: var(--title);
  }

  button {
    cursor: pointer;
  }

  p {
    font-size: 1.25rem;
  }

  .welcome-text {
    width: 40rem;
    line-height: 1.5;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .welcome-text h1 {
    font-size: 2.5rem;
  }

  .welcome-text p {
    color: var(--paragraph);
  }

  .welcome {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .welcome button {
    background-color: transparent;
    padding: 0.5rem 5rem;
    border: 2px solid var(--brand-purple);
    border-radius: 5rem;
    color: var(--brand-purple);
    transition: 0.2s;
  }

  .welcome button:hover {
    background-color: var(--brand-purple);
    color: white;
    box-shadow: 5px 5px 0px var(--brand-purple-shadow);
    transition: 0.2s;
  }



  #goals {
    padding-bottom: 7rem;
  }

  #goals .cards {
    display: flex;
    flex-direction: row;
    width: fit-content;
    margin: 0 auto;
    margin-top: 8rem;
    gap: 2rem;
    margin-bottom: 5rem;
  }

  #goals .footer {
    margin: 0 auto;
    margin-top: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 1rem;
  }

  #goals .footer a {
    transition: 0.2s;
    align-self: center;
  }

  #goals .footer a:hover {
    transform: translateY(0.2rem);
  }

  #specializations .cards {
    margin-top: 7rem;
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  #about h2 {
    text-align: left;
  }

  #about {
    display: flex;
    justify-content: center;
    padding-top: 0;
  }

  #about .text {
    width: 34rem;
  }

  #about .text h2 {
    font-size: 2.5rem;
  }

  #about .text p {
    color: var(--paragraph);
    font-size: 1.125rem;
  }

  #about .bio {
    display: flex;
    margin-top: 2.5rem;
    flex-direction: column;
    gap: 1rem;
  }

  #about .content {
    display: flex;
    justify-content: space-between;
  }

  #about .content img {
    width: 26rem;
    border: 1px solid var(--brand-purple);
    border-radius: 50%;
    transition: .5s;
  }

  #about .content img:hover {
    transform: scale(1.05);
    box-shadow: 10px 10px 0px var(--brand-purple-shadow-lighter);
  }

  #contact {
    padding-top: 0;
    height: 100vh;
    display: flex;
    align-items: center;
    flex-direction: row;
    align-items: center;
  }

  #contact .content {
    display: flex;
    justify-content: space-between;
  }

  #contact .content img {
    border-radius: 20px;
    box-shadow: 10px 10px 0px var(--brand-purple-shadow-light);
  }

  #contact .content .text {
    display: flex;
    text-align: right;
    flex-direction: column;
    gap: 2.25rem;
    align-items: flex-end;
  }

  #contact .content .text h2 {
    font-size: 2rem;
  }

  #contact .content .text p {
    font-size: 1.125rem;
    width: 30rem;
  }

  #contact .content .text a {
    text-decoration: none;
  }

  #contact .content .text button {
    background-color: transparent;
    padding: 0.5rem 2rem;
    border: 2px solid var(--brand-purple);
    border-radius: 20px;
    font-size: 1.25rem;
    font-weight: 700;
    color: var(--brand-purple);
    transition: 0.2s;
    align-items: center;

    display: flex;
    gap: 1.875rem;
  }

  #contact .content .text button:hover {
    background-color: var(--brand-purple);
    color: white;
    box-shadow: 5px 5px 0px var(--brand-purple-shadow);
    transition: 0.2s;
  }
}

@media only screen and (max-width: 991px) {
  html {
    font-size: 87.5%;
  }
  .wrapper {
    width: 85%;
    margin: 0 auto;
  }
  
}
</style>
