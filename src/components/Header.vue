<template>
  <div class="menu-btn" @click="handleClick" :class="{ close: close }">
    <div class="btn-line"></div>
    <div class="btn-line"></div>
    <div class="btn-line"></div>
  </div>
  <nav class="menu" :class="{ show: show }">
    <div class="menu-branding" :class="{ show: show }">
      <div class="portrait"></div>
    </div>
    <ul class="menu-nav" :class="{ show: show }">
      <li class="nav-item" @click.prevent="handleClick">
        <router-link :to="{ name: 'Home' }" class="nav-link">Home</router-link>
      </li>
      <li class="nav-item" @click.prevent="handleClick">
        <router-link :to="{ name: 'About' }" class="nav-link"
          >About</router-link
        >
      </li>
      <li class="nav-item" @click.prevent="handleClick">
        <router-link :to="{ name: 'Work' }" class="nav-link">Work</router-link>
      </li>
      <li class="nav-item" @click.prevent="handleClick">
        <router-link :to="{ name: 'Contact' }" class="nav-link"
          >Contact</router-link
        >
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      close: false,
    };
  },
  methods: {
    handleClick() {
      if (!this.show) {
        this.show = true;
        this.close = true;
      } else {
        this.show = false;
        this.close = false;
      }
    },
  },
};
</script>

<style scoped>
a.router-link-active {
  color: #eece1a;
}
.menu-btn {
  position: absolute;
  z-index: 3;
  right: 35px;
  top: 35px;
  cursor: pointer;
  transition: all 0.7s ease-out;
}
.menu-btn .btn-line {
  width: 28px;
  height: 3px;
  margin: 0 0 5px 0;
  background: #fff;
  transition: all 0.7s ease-out;
}
.menu-btn.close {
  transform: rotate(180deg);
}
.menu-btn.close .btn-line:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}
.menu-btn.close .btn-line:nth-child(2) {
  opacity: 0;
}
.menu-btn.close .btn-line:nth-child(3) {
  transform: rotate(-45deg) translate(7px, -6px);
}

.menu {
  position: fixed;
  top: 0;
  width: 100%;
  opacity: 0.99999;
  visibility: hidden;
}
.menu.show {
  visibility: visible;
}
.menu-branding,
.menu-nav {
  display: flex;
  flex-flow: column wrap;
  align-items: center;
  justify-content: center;
  float: left;
  width: 50%;
  height: 100vh;
  overflow: hidden;
}
.menu-nav {
  margin: 0;
  padding: 0;
  background: #1a1c1e;
  list-style: none;
  transform: translate3d(0, -100%, 0);
  transition: all 0.7s ease-out;
}
.menu-nav.show {
  transform: translate3d(0, 0, 0);
}
.menu-branding {
  background: #26292c;
  transform: translate3d(0, 100%, 0);
  transition: all 0.7s ease-out;
}
.menu-branding.show {
  transform: translate3d(0, 0, 0);
}
.menu-branding .portrait {
  width: 250px;
  height: 250px;
  /* background: url("../img/Me-11.jpg"); */
  border-radius: 50%;
  border: solid 3px #eece1a;
}
.menu .nav-item.show {
  transform: translate3d(0, 0, 0);
}
.menu .nav-link {
  display: inline-block;
  position: relative;
  font-size: 30px;
  text-transform: uppercase;
  padding: 1rem 0;
  font-weight: 300;
  /* color: #fff; */
  text-decoration: none;
  transition: all 0.7s ease-out;
}
.menu .nav-link:hover {
  color: #eece1a;
}

.nav-item:nth-child(1) {
  transition-delay: 0.1s;
}

.nav-item:nth-child(2) {
  transition-delay: 0.2s;
}

.nav-item:nth-child(3) {
  transition-delay: 0.3s;
}

.nav-item:nth-child(4) {
  transition-delay: 0.4s;
}
</style>
