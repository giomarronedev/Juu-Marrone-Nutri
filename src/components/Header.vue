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
      <button @click="isMenu = true">
        <font-awesome-icon icon="fa-solid fa-bars" class="fa-2xl" />
      </button>
      <div v-if="isMenu == true">
        <div class="menu">
          <button @click="isMenu = false"><font-awesome-icon icon="fa-solid fa-x" class="fa-xl"/></button>
          <h2>Juu<span>Marrone</span></h2>
          <ul>
            <a @click="isMenu = false" href="#">Início</a>
            <a @click="isMenu = false" href="#goals">Seus objetivos</a>
            <a @click="isMenu = false" href="#specializations">Especializações</a>
            <a @click="isMenu = false" href="#about">Sobre</a>
          </ul>
          <div class="social">
            <a target="_blank" href="https://www.instagram.com/jumarrone.nutri/"><font-awesome-icon icon="fa-brands fa-instagram" class="fa-2xl"/> <p>@jumarrone.nutri</p></a>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      isMenu: false
    }
  }
};
</script>

<style scoped>
@media only screen and (min-width: 992px) {
  header .mobile {
    display: none;
  }
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
    color: var(--title);
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
    position: sticky;
    top: 0;
    z-index: 100;
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
    font-weight: 700;
  }

  p {
    font-size: 1.5rem;
    font-weight: 500;
    color: var(--title);
  }

  header button {
    line-height: 0;
    background-color: transparent;
    color: white;
    border: none;
  }

  .menu {
    position: fixed;
    height: 100vh;
    width: 100vw;
    left: 0;
    top: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    justify-content: space-around;
    background-color: var(--brand-purple);
  }

  .menu h2 {
    color: var(--brand-purple-shadow-light);
    font-size: 2rem;
  } 

  .menu ul {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    text-align: center;
  }

  .menu ul a {
    color: white;
    text-decoration: none;
    font-weight: 700;
    font-size: 1.5rem;
    width: 100vw;
    padding-block: 1rem;
    border: 1px solid transparent;
  }

  .menu ul a:active {
    background-color: var(--brand-purple-shadow);
    border-block: 1px solid white;
  }

  .menu .social a, .menu .social a p {
    color: white;
  }
  .menu .social a {
    width: 100vw;
    padding: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid transparent;
  }

  .menu .social a:active {
    background-color: var(--brand-purple-shadow);
    border-block: 1px solid white;
  }

  .menu .social a p {
    display: flex;
  }

  .menu .social {
    margin-bottom: 2rem;
  }
  
  .menu .social a {
    display: flex;
    gap: 1rem;
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: 700;
  }
  .menu button {
    position: absolute;
    top: 2rem;
    right: 2rem;
  }
}
</style>
