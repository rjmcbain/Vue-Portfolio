<template>
  <div id="main">
    <main id="home">
      <h1 class="lg-heading">
        RJ
        <span class="text-secondary">McBain</span>
      </h1>
      <h2 class="sm-heading">
        Front End Developer
      </h2>
      <div class="icons">
        <a href="https://github.com/rjmcbain" target="_blank">
          <i class="fab fa-github fa-2x"></i>
        </a>
        <a href="https://www.linkedin.com/in/rjmcbain/" target="_blank">
          <i class="fab fa-linkedin fa-2x"></i>
        </a>
        <a href="mailto:rmcbain01@gmail.com">
          <i class="fab fa fa-envelope fa-2x"></i>
        </a>
        <a
          href="https://www.instagram.com/rjmcbainphotography/"
          target="_blank"
        >
          <i class="fab fa-instagram fa-2x"></i>
        </a>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
};
</script>

<style scoped>
#main::before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  background-image: url("../assets/images/background.jpg");
  background-attachment: fixed;
  background-size: cover;
  opacity: 0.25;
}
</style>
