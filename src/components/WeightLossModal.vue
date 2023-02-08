<template>
  <main>
    <div class="modal">
      <header>
        <div class="title-area">
          <h1>Perda de peso</h1>
          <h2>Eficaz e saudável</h2>
        </div>
        <button @click="this.closeModal">
          <font-awesome-icon icon="fa-solid fa-x" class="fa-xl" />
        </button>
      </header>
      <div class="image"></div>
      <div class="description">
        <p>
          É possível ser acima do peso e saudável? Sem sombra de dúvidas de que
          sim. Porém, é inegável que a obesidade é uma doença que,
          principalmente em casos ameaçadores, deve ser tratada.
        </p>
        <p>
          Além disso, é perfeitamente normal que uma pessoa queira perder peso
          por questões de autoestima. Acontece que em muitos casos, a perda de
          peso pode ser feita de forma perigosa e irresponsável. Por isso, uma
          dieta balanceada e uma reeducação alimentar (se necessária) é a base
          para um emagrecimento saudável e sem recaídas 💜.
        </p>
      </div>
    </div>
  </main>
</template>
<script>
export default {
  name: "WeightLossModal",

  emits: ["closeWeightModal"],

  methods: {
    closeModal() {
      this.$emit("closeWeightModal");
    },
  }
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
  background-image: url("../assets/perda-de-peso-modal.png");
  background-size: cover;
  background-position: 70%;
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
</style>
