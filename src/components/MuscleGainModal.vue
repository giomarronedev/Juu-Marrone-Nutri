<template>
  <main>
    <div class="modal">
      <header>
        <div class="title-area">
          <h1>Ganho de massa</h1>
          <h2>Força e resistência</h2>
        </div>
        <button @click="this.closeModal">
          <font-awesome-icon icon="fa-solid fa-x" class="fa-xl" />
        </button>
      </header>
      <div class="image"></div>
      <div class="description">
        <p>
          Ter músculos desenvolvidos pode ser importante dependendo do que uma
          pessoa quer que seu corpo seja capaz de fazer. E crescer de forma
          saudável é extremamente importante para que futuramente você não sofra
          recaídas e mantenha o tão famoso
          <span><strong>shape</strong></span> 💪.
        </p>
        <p class="not-on-mobile">
          Uma pessoa pode querer desenvolver seus músculos por diversos motivos,
          como para performance em atividades físicas, ganho de força ou até
          mesmo por pura estética. Mas saiba que seja qual for a sua motivação,
          crescer da maneira certa é crucial para que você desenvolva seus
          músculos de forma saudável, e é aí que eu entro pra te ajudar!
        </p>
      </div>
    </div>
  </main>
</template>
<script>
export default {
  name: "MuscleGainModal",

  methods: {
    closeModal() {
      this.$emit("closeMuscleModal");
    },
  },
};
</script>
<style scoped>
main {
  background-color: rgba(0, 0, 0, 0.2);
  position: fixed;
  top: 0;
  height: 100%;
  width: 100%;
  z-index: 100;
  backdrop-filter: blur(10px);
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal {
  padding: 1rem 0rem 2rem;
  width: 70rem;
  height: 48.5rem;
  max-height: 80%;
  background-color: white;
  border-radius: 30px;
  border: 1px solid var(--brand-purple);

  display: flex;
  flex-direction: column;
  align-items: center;
}
header {
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  width: 100%;
}

header button {
  position: absolute;
  right: 3rem;
  line-height: 0;
  color: var(--brand-purple);
  background-color: transparent;
  border-radius: 100%;
  padding: 0.5rem;
  border: none;
  transition: 0.3s;
}

header button:hover {
  transform: scale(1.1);
}

.title-area h1 {
  color: var(--brand-purple);
  font-size: 3rem;
}

.title-area h2 {
  margin-top: -1rem;
  text-align: right;
  margin-right: -4rem;
  color: var(--title);
  opacity: 0.8;
}

.image {
  width: 90%;
  height: 19rem;
  border-radius: 20px;
  margin-top: 2rem;
  margin-bottom: 3rem;
  background-image: url("../assets/ganho-massa-modal.jpg");
  background-size: cover;
  background-position: 70% 40%;
  border: 1px solid var(--brand-purple);
}

.description {
  color: var(--paragraph);
  text-align: center;
  width: 50rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.description p {
  font-size: 1rem;
}

@media only screen and (max-width: 991px) {
  main {
    background-color: rgba(0, 0, 0, 0.2);
    position: fixed;
    top: 0;
    height: 100%;
    width: 100%;
    z-index: 100;
    backdrop-filter: blur(10px);
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .modal {
    padding: 1rem 0rem 2rem;
    width: 90%;
    height: fit-content;
    max-height: 80%;
    background-color: white;
    border-radius: 30px;
    border: 1px solid var(--brand-purple);
    padding-inline: 1rem;

    display: flex;
    flex-direction: column;
    align-items: center;
  }
  header {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    width: 100%;
  }

  header button {
    position: absolute;
    right: 1rem;
    top: 0;
    line-height: 0;
    color: var(--brand-purple);
    background-color: transparent;
    border-radius: 100%;
    padding: 0.5rem;
    border: none;
    transition: 0.3s;
  }

  header button:hover {
    transform: scale(1.1);
  }

  .title-area h1 {
    color: var(--brand-purple);
    font-size: 2rem;
    margin-top: 2rem;
  }

  .title-area h2 {
    margin-top: -.8rem;
    text-align: right;
    margin-right: 0;
    color: var(--title);
    opacity: 0.8;
    font-size: 1.2rem;
  }

  .image {
    width: 90%;
    height: 10rem;
    border-radius: 20px;
    margin-top: 1rem;
    margin-bottom: 1rem;
    background-image: url("../assets/ganho-massa-modal.jpg");
    background-size: cover;
    background-position: 70% 40%;
    border: 1px solid var(--brand-purple);
  }

  .description {
    color: var(--paragraph);
    text-align: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .description p {
    font-size: 1rem;
  }
  .not-on-mobile {
    display: none;
  }
}
</style>
