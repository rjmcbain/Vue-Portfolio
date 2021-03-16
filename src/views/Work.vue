<template>
  <main id="work">
    <h1 class="lg-heading">
      My
      <span class="text-secondary">Work</span>
    </h1>
    <h2 class="sm-heading">
      Check out some of my projects...
    </h2>
    <Projects />
  </main>
</template>

<script>
import Projects from "../components/Projects";
export default {
  components: {
    Projects,
  },
};
</script>

<style></style>
