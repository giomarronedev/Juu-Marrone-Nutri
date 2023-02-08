<template>
  <header id="header">
    <div class="wrapper desktop">
      <p>Juu<span>Marrone</span></p>
      <ul>
        <a href="#">Início</a>
        <a href="#goals">Seus objetivos</a>
        <a href="#specializations">Especializações</a>
        <a href="#about">Sobre</a>
      </ul>
      <a href="#contact"><button>Agende sua consulta</button></a>
    </div>
    <div class="wrapper mobile">
      <p>Juu<span>Marrone</span></p>
      <ul>
        <a href="#">Início</a>
        <a href="#goals">Seus objetivos</a>
        <a href="#specializations">Especializações</a>
        <a href="#about">Sobre</a>
      </ul>
      <button><font-awesome-icon icon="fa-solid fa-bars"/></button>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<style scoped>
@media only screen and (min-width: 992px) {
  .wrapper {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100%;
  }

  header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1.5rem 0;
    position: sticky;
    top: 0;
    background-color: #faf1ff;
    z-index: 10;
    border-bottom: 2px solid var(--brand-purple);
  }

  p {
    font-size: 2rem;
    font-size: 500;
    user-select: none;
  }

  span {
    font-weight: bold;
  }

  ul {
    display: flex;
    gap: 2rem;
  }

  a {
    color: var(--title);
    text-decoration: none;
    transition: 0.2s;
    font-size: 1rem;
    font-weight: 500;
    color: var(--title)
  }

  a:hover {
    color: var(--brand-purple);
    transition: 0.2s;
  }

  button {
    background-color: transparent;
    padding: 0.5rem 3rem;
    border: 2px solid var(--brand-purple);
    border-radius: 5rem;
    color: var(--brand-purple);
    transition: 0.2s;
  }

  button:hover {
    background-color: var(--brand-purple);
    color: white;
    box-shadow: 5px 5px 0px var(--brand-purple-shadow);
    transition: 0.2s;
  }
}

@media only screen and (max-width: 991px) {
  header {
    background-color: var(--brand-purple);
    padding: 1rem 0;
  }

  header .wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  header .desktop {
    display: none;
  }

  span {
    color: white;
  }

  ul {
    display: none;
  }

  p {
    font-size: 1.5rem;
  }

}
</style>
