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
  background-color: #121212;
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
  width: 100%;
  max-width: 1200px;
}

.gradient-btn {
  position: relative;
  display: inline-block;
  color: #fff;
  background: #121212;
  font-family: "Open Sans", sans-serif;
  font-size: 18px;
  line-height: 27px;
  padding: 14px 46px;
  margin: 2px;
  text-decoration: none;
  // border-radius: 0 2rem 0 2rem;

  &::before {
    content: "";
    position: absolute;
    top: -2px;
    left: -2px;
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    background: linear-gradient(90deg, #369aff, #ff658a);
    // border-radius: 0 2rem 0 2rem;
    z-index: -1;
  }
}

.link {
  position: relative;
  color: #fff;
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
  }
}
</style>
