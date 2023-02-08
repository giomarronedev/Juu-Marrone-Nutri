<template>
  <main id="card">
    <div class="text">
      <h3>{{ title }}</h3>
      <p>{{ content }}</p>
    </div>
    <img :src="image" :alt="alt" />
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
main {
  width: 100%;
  height: fit-content;
  border: 1px solid var(--brand-purple);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  overflow: hidden;
  background: linear-gradient(270deg, rgba(250, 48, 48, 0) 34.51%, rgba(158, 0, 255, 0.066) 100%);
  transition: .5s;
  cursor: pointer;
  backdrop-filter: blur(3px);
}

main:hover {
    transform: translateX(2rem);
    box-shadow: 0px 0px 5px var(--brand-purple);
}

.text {
    padding: 0.8rem 0 0.8rem 1.25rem;
}

h3 {
  font-size: 1.4rem;
  color: var(--title);
}
p {
  margin-top: 0.5rem;
  font-size: 1rem;
  width: 100%;
  color: var(--paragraph);
  line-height: 1.5;
}

img {
  border-top-left-radius: 30px 90%;
  border-bottom-left-radius: 30px 90%;
  margin-left: 4rem;
  margin-right: -3rem;
  height: 100%;
  width: 22rem;
  object-fit: cover;
}
</style>
