<template>
  <nav
    class="navbar fixed-top navbar-expand-md navbar-dark shadow-none"
    :style="changeColor"
  >
    <!-- Container wrapper -->
    <div class="container-fluid">
      <!-- Navbar brand -->
      <nuxt-link to="/" class="navbar-brand" tag="a">Jchann24</nuxt-link>

      <!-- Toggle button -->
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarContent"
        aria-controls="navbarContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <i class="fas fa-bars"></i>
      </button>

      <!-- Collapsible wrapper -->
      <div id="navbarContent" class="collapse navbar-collapse">
        <!-- Left links -->
        <ul class="navbar-nav ml-auto mb-2 mb-lg-0">
          <!-- Navbar dropdown -->
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="#">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="#">Contact</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      scrollPosition: null
    }
  },
  computed: {
    changeColor() {
      return this.scrollPosition > 30
        ? 'background-color: #282A36; transition: background-color 600ms ease'
        : ''
    }
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll)
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY
    }
  }
}
</script>

<style scoped></style>
