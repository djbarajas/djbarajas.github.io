<template>
  <nav class="navbar is-transparent" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">

      <a role="button" class="navbar-burger"
         aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div id="navbarBasicExample" class="navbar-menu is-transparent is-shadowless">
      <div class="navbar-start">
        <a href="#about" class="navbar-item has-text-white">
          About Me
        </a>

        <a href="#projects" class="navbar-item has-text-white">
          Projects
        </a>

        <a href="#more" class="navbar-item has-text-white">
          More Information
        </a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'TheNavbar',
  mounted() {
    // Get all "navbar-burger" elements
    const $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);

    // Check if there are any navbar burgers
    if ($navbarBurgers.length > 0) {
      // Add a click event on each of them
      $navbarBurgers.forEach((el) => {
        el.addEventListener('click', () => {
          // Get the target from the "data-target" attribute
          const { target } = el.dataset;
          const $target = document.getElementById(target);

          // Toggle the "is-active" class on both the "navbar-burger" and the "navbar-menu"
          el.classList.toggle('is-active');
          $target.classList.toggle('is-active');
        });
      });
    }
  },
};
</script>

<style scoped>
.is-transparent {
  background: transparent !important;
}
.navbar-burger {
  color: white;
}
.navbar-item:hover {
  background: #2c3e50;
}
</style>
