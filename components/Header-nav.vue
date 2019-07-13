<template>
    <nav
      class="navbar header has-shadow is-primary"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <a
          class="navbar-item"
          href="/"
        >
          <img
            src="~assets/buefy.png"
            alt="Buefy"
            height="28"
          >
        </a>

        <div
          class="navbar-burger"
          @click="toogleMenu">
          <span />
          <span />
          <span />
        </div>
      </div>
    </nav>
</template>

<script>
export default {
  name: 'header-nav',
  methods: {
    toogleMenu() {
      const menu = document.getElementsByClassName('section-menu');
      menu[0].classList.toggle('show-menu')
    },
  },
}
</script>

<style lang="sass" scoped>
.navbar-burger
  display: none;
@media (max-width: 768px)
    .navbar-burger
      display: block;
</style>

