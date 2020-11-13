<template>
  <div>
    <Navbar />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import Navbar from "./../components/Navbar";
import Footer from "./../components/Footer";

export default {
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style lang="scss">
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  // outline: 1px solid rgba(255, 0, 0, 0.3);
}

html,
body {
  width: 100%;
  height: 100%;
  background-color: #0D0D0D;
}

html {
  font-family: "Open Sans" sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}

.container {
  position: relative;
  width: 100%;
  max-width: 1200px;
}

.gradient-btn {
  position: relative;
  display: inline-block;
  color: #f8f8f8;
  background: #0D0D0D;
  font-family: "Open Sans", sans-serif;
  font-size: 18px;
  line-height: 27px;
  padding: 14px 46px;
  margin: 2px;
  text-decoration: none;
  // border-radius: 0 2rem 0 2rem;
  z-index: 1;

  &::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #0D0D0D;
    // border-radius: 0 2rem 0 2rem;
    z-index: -1;
  }

  &::before {
    content: "";
    position: absolute;
    top: -2px;
    left: -2px;
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    background: linear-gradient(90deg, #369aff, #ff658a);
    background-size: 150%;
    background-position: center left;
    // border-radius: 0 2rem 0 2rem;
    z-index: -2;
    transition: 0.2s ease-in-out all;
  }

  &:hover::before {
    background-position: center right;
  }
}

.link {
  position: relative;
  color: #f8f8f8;
  font-family: "Open Sans", sans-serif;
  font-size: 18px;
  font-weight: 500;
  line-height: 24px;
  text-decoration: none;

  &::before {
    content: "";
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    height: 2px;
    background: linear-gradient(90deg, #369aff, #ff658a);
    background-size: 150%;
    background-position: center left;
    transition: 0.2s ease-in-out all;
  }

  &:hover::before {
    background-position: center right;
  }
}

// PAGE TRANSITIONS
.page-enter-active,
.page-leave-active {
  transition: all 0.5s ease-in-out;
}

.page-enter,
.page-leave-active {
  opacity: 0;
}

// MEDIA QUERIES
@media (max-width: 576px) {
  .container {
    margin: 0 24px;
  }
}

@media (min-width: 577px) and (max-width: 1199px) {
  .container {
    margin: 0 10%;
  }
}

@media (min-width: 1200px) {
  .container {
    margin: 0 10%;
  }
}
</style>
