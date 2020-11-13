<template>
  <header class="navbar">
    <div class="container">
      <h1 class="logo"><NuxtLink to="/">logo</NuxtLink></h1>
      <nav class="nav">
        <ul>
          <li><NuxtLink to="/about">about</NuxtLink></li>
          <li><NuxtLink to="/work">work</NuxtLink></li>
          <li><NuxtLink to="#">contact</NuxtLink></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style lang="scss" scoped>
.navbar {
  background-color: #0d0d0d;
  width: 100%;
  height: 100px;
  display: flex;
  justify-content: center;
  position: relative;

  .container {
    height: 100px;
    width: 100%;
    max-width: 1200px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;

    .logo {
      font-family: "Poppins", sans-serif;
      font-size: 1.5rem;
      font-weight: 500;
      line-height: 32px;

      a {
        color: #f8f8f8;
        text-decoration: none;
      }
    }

    .nav {
      ul {
        list-style-type: none;
        display: flex;
        flex-direction: row;

        li {
          margin-left: 48px;

          a {
            position: relative;
            font-family: "Poppins", sans-serif;
            font-size: 1rem;
            font-weight: 400;
            line-height: 1.5rem;
            color: #f8f8f8;
            text-decoration: none;

            &::before {
              content: "";
              position: absolute;
              top: 100%;
              left: 0;
              height: 2px;
              width: 0;
              background: linear-gradient(90deg, #369aff, #ff658a);
              transition: width 0.2s ease-in-out;
            }

            &:hover::before {
              width: 100%;
            }
          }
        }
      }
    }
  }
}

@media (max-width: 768px) {
  .container {
    margin: 0 24px;
  }

  .nav {
    display: none;
  }
}
</style>
