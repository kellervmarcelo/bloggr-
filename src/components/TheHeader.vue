<template>
  <header class="red-gradient container">
    <div class="app-header__small-screen">
      <img class="app-header__logo" src="../assets/img/logo.svg" alt="Bloggr Logo" />
      <img
        class="app-header__icon"
        :src="
          isMenuOpen
            ? require('../assets/img/icon-close.svg')
            : require('../assets/img/icon-hamburger.svg')
        "
        role="button"
        @click="isMenuOpen = !isMenuOpen"
      />
    </div>

    <div class="app-header__small-screen--open bg-white" v-if="isMenuOpen">
      <nav class="flex-center">
        <ul class="app-header__links font-overpass font-bold">
          <li>Product</li>
          <li>Company</li>
          <li>Connect</li>
        </ul>
      </nav>

      <hr />

      <div>
        <a href="#">Login</a>
        <button>Sign Up</button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'TheHeader',
  data() {
    return {
      isMenuOpen: false,
      closeIcon: '../assets/img/icon-close.svg',
      hamburguerIcon: null,
    };
  },
};
</script>

<style lang="scss" scoped>
.app-header {
  &__small-screen {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;

    padding: 4rem 0;

    &--open {
      background: #fff;
      padding: 2rem 0;
    }
  }

  &__logo {
    height: 30px;
  }

  &__icon {
    height: 18px;
    width: auto;
  }

  &__links {
    list-style: none;
    font-size: 1.25rem;

    li + li {
      margin-top: 2rem;
    }
  }
}
</style>
