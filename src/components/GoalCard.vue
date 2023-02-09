<template>
  <main>
    <img :src="image" :alt="alt" />
    <h3>{{ title }}</h3>
    <p>{{ content }}</p>
  </main>
</template>
<script>
export default {
  name: "GoalCard",

  props: {
    image: {
      type: String,
      required: false,
    },
    alt: {
      type: String,
      required: false,
    },
    title: {
      type: String,
      required: true,
    },
    content: {
      type: String,
      required: true,
    },
  },
};
</script>
<style scoped>
@media only screen and (min-width: 992px) {
  main {
    width: 16rem;
    height: 24.5rem;
    border: 1px solid var(--brand-purple);
    border-radius: 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem;
    text-align: center;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0) 0.37%, rgba(158, 0, 255, 0.04) 100%);
    gap: 1rem;
    transition: .5s;
    cursor: pointer;
    backdrop-filter: blur(3px);
  }

  main:hover {
    transform: translateY(-2rem);
    box-shadow: 0px 0px 5px var(--brand-purple);
  }

  img {
    border-radius: 1rem;
    width: 100%;
  }

  p {
    color: var(--paragraph);
    font-size: 1rem;
  }
}
@media only screen and (max-width: 991px) {
  main {
    width: 80%;
    max-width: 25rem;
    height: fit-content;
    border: 1px solid var(--brand-purple);
    border-radius: 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem;
    text-align: center;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0) 0.37%, rgba(158, 0, 255, 0.04) 100%);
    gap: 1rem;
    transition: .2s;
    cursor: pointer;
    backdrop-filter: blur(3px);
    margin: 0 auto;
  }

  main:active {
    /* transform: translateY(-2rem); */
    transform: scale(1.1);
    box-shadow: 0px 0px 5px var(--brand-purple);
  }

  img {
    border-radius: 1rem;
    width: 100%;
  }

  p {
    color: var(--paragraph);
    font-size: 1rem;
  }
}
</style>
