<template>
  <div>
    <!-- HERO -->
    <section class="about__hero">
      <div class="container">
        <h1 class="about__hero--title">
          <span>web development</span> <span>& design</span>
        </h1>
        <p class="about__hero--desc">
          Some lengthy description about what I do and how I can help in massive
          text that spans the entire width of the container for whatever reason
          because it's the trendy thing to do nowadays.
        </p>
      </div>
    </section>
    <!-- CLIENTS -->
    <section class="about__clients">
      <div class="container">
        <div class="about__clients--grid">
          <div class="client">
            <img
              src="~/assets/AXIOM-logo.png"
              alt="AXIOM Architecture logo"
              class="client__logo"
            />
          </div>
          <div class="client">
            <img
              src="~/assets/Phoebe-logo.png"
              alt="Phoebe for Mayor logo"
              class="client__logo"
            />
          </div>
          <div class="client">
            <img
              src="~/assets/DJ-logo.png"
              alt="DJ Johnson for State Rep logo"
              class="client__logo"
            />
          </div>
          <div class="client">
            <img
              src="~/assets/ISAF-logo.png"
              alt="Issac Sterett Adventure Foundation logo"
              class="client__logo"
            />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.about__hero {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  margin: 200px 0;

  &--title {
    display: flex;
    flex-direction: column;
    color: #f8f8f8;
    font-family: "Poppins", sans-serif;
    font-size: 48px;
    line-height: 72px;
    font-weight: 500;
    text-align: left;
  }

  &--desc {
    position: relative;
    color: #f8f8f8;
    font-family: "Open Sans", sans-serif;
    font-size: 20px;
    line-height: 32px;
    max-width: 75%;
    margin: 48px 0 0 0;

    &::before {
      content: "";
      width: 100px;
      height: 2px;
      position: absolute;
      left: 0px;
      top: -24px;
      background: linear-gradient(90deg, #ff658a, #369aff);
    }
  }
}

.about__clients {
  display: flex;
  // align-items: flex-start;
  justify-content: center;
  width: 100%;
  margin-bottom: 200px;

  &--grid {
    display: grid;
    width: 100%;
    grid-template-columns: repeat(4, 25%);
    grid-auto-rows: auto;

    .client {
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 40px;

      &__logo {
        width: 100%;
      }
    }
  }
}

// MEDIA QUERIES
@media (max-width: 576px) {
  .about__hero {
    text-align: center;

    &--title {
      font-size: 32px;
      line-height: 48px;
      font-weight: 500;
    }

    &--desc {
      max-width: 100%;
      line-height: 1.5;
      text-align: left;
    }
  }

  .about__clients {
    &--grid {
      grid-template-columns: repeat(2, 50%);

      .client {
        padding: 32px;
      }
    }
  }
}

@media (min-width: 577px) and (max-width: 1199px) {
  .about__hero {
    text-align: center;

    &--title {
      font-size: 32px;
      line-height: 48px;
      font-weight: 500;
      text-align: center;
    }

    &--desc {
      max-width: 100%;
      line-height: 1.5;
      text-align: center;

      &::before {
        left: 50%;
        transform: translateX(-50%);
      }
    }
  }

  .about__clients {
    &--grid {
      .client {
        padding: 16px;
      }
    }
  }
}
</style>
