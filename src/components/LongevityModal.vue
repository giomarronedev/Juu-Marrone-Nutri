<template>
    <main>
      <div class="modal">
        <header>
          <div class="title-area">
            <h1>Longevidade</h1>
            <h2>Saúde e bem estar</h2>
          </div>
          <button @click="this.closeModal">
            <font-awesome-icon icon="fa-solid fa-x" class="fa-xl" />
          </button>
        </header>
        <div class="image"></div>
        <div class="description">
          <p class="not-on-mobile">
            O corpo humano pode ser visto como uma máquina que, se não for bem cuidada com o tempo, apresentará defeitos mais cedo. Por isso, uma alimentação visando a longevidade é extremamente importante para quem se preocupa com o <span><strong>futuro</strong></span>.
          </p>
          <p>
            Aderir a uma alimentação que visa a <span><strong>longevidade</strong></span> dá à pessoa não apenas o benefício da saúde melhorada, mas também do bem estar no dia-a-dia. Deixando você mais disposto(a) para aproveitar bons momentos com sua família ❤️.
          </p>
        </div>
      </div>
    </main>
  </template>
  <script>
  export default {
    name: "LongevityModal",
    
    methods: {
      closeModal() {
        this.$emit("closeLongevityModal");
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
    background-image: url("../assets/longevidade-modal.jpg");
    background-size: cover;
    background-position: 50% 50%;
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
    margin-top: -.4rem;
    text-align: right;
    margin-right: 0;
    color: var(--title);
    opacity: 0.8;
    font-size: 1.2rem;
  }

  .image {
    width: 90%;
    height: 10rem;
    margin-top: 1rem;
    margin-bottom: 1rem;
    background-image: url("../assets/longevidade-modal.jpg");
    background-size: cover;
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
  