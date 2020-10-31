<template>
  <header class="navbar">
    <div class="container">
      <h1 class="logo"><a href="#">logo</a></h1>
      <nav class="nav">
        <ul>
          <li><a href="#">about</a></li>
          <li><a href="#">work</a></li>
          <li><a href="#">blog</a></li>
          <li><a href="#">contact</a></li>
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
  background-color: #121212;
  height: 100px;
  display: flex;
  justify-content: center;
  position: relative;

  .container {
    height: 100px;
    width: 100%;
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
        color: #fff;
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
            color: #fff;
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
