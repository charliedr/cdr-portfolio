<template>
  <div>
    <!-- HERO -->
    <section class="hero">
      <div class="container">
        <h1 class="hero__title">hero heading</h1>
        <p class="hero__desc">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid earum
          suscipit veritatis perspiciatis reprehenderit atque sed praesentium
          doloribus.
        </p>
        <a href="#" class="gradient-btn">contact button</a>
      </div>
    </section>
    <!-- SHOWCASE -->
    <section class="showcase">
      <div class="container">
        <div class="showcase__pic">
          <img src="@/assets/iphone-front.png" alt="iPhone mockup" />
        </div>
      </div>
    </section>
    <!-- ABOUT SNIPPET -->
    <section class="about-me">
      <div class="container">
        <p class="about-me__text">
          Some lengthy description about what I do and how I can help in massive
          text that spans the entire width of the container for whatever reason
          because it's the trendy thing to do nowadays. Lorem ipsum dolor sit
          amet consectetur adipisicing elit.
        </p>
        <NuxtLink to="/about" class="link">link to about page</NuxtLink>
      </div>
    </section>
    <!-- WORK -->
    <section class="my-work">
      <div class="container">
        <div class="my-work__header">
          <h1 class="my-work__title">work</h1>
          <NuxtLink to="/work" class="link">link to work page</NuxtLink>
        </div>
        <div class="my-work__grid">
          <div class="card">
            <div class="card__img">
              <a href="#">
                <img src="@/assets/iphone.png" alt="iPhone mockup" />
              </a>
            </div>
            <div class="card__content">
              <div class="card__content--title">Phoebe For Mayor</div>
              <div class="card__content--services">
                web design, web development
              </div>
            </div>
          </div>
          <div class="card">
            <div class="card__img">
              <a href="#">
                <img src="@/assets/iphone.png" alt="iPhone mockup" />
              </a>
            </div>
            <div class="card__content">
              <div class="card__content--title">DJ Johnson For State Rep</div>
              <div class="card__content--services">
                web design, web development
              </div>
            </div>
          </div>
          <div class="card">
            <div class="card__img">
              <a href="#">
                <img src="@/assets/iphone.png" alt="iPhone mockup" />
              </a>
            </div>
            <div class="card__content">
              <div class="card__content--title">AXIOM Architecture</div>
              <div class="card__content--services">
                web design, web development, typography
              </div>
            </div>
          </div>
          <div class="card">
            <div class="card__img">
              <a href="#">
                <img src="@/assets/iphone.png" alt="iPhone mockup" />
              </a>
            </div>
            <div class="card__content">
              <div class="card__content--title">company name</div>
              <div class="card__content--services">web design, strategy</div>
            </div>
          </div>
          <div class="card">
            <div class="card__img">
              <a href="#">
                <img src="@/assets/iphone.png" alt="iPhone mockup" />
              </a>
            </div>
            <div class="card__content">
              <div class="card__content--title">company name</div>
              <div class="card__content--services">web design, strategy</div>
            </div>
          </div>
          <div class="card">
            <div class="card__img">
              <a href="#">
                <img src="@/assets/iphone.png" alt="iPhone mockup" />
              </a>
            </div>
            <div class="card__content">
              <div class="card__content--title">company name</div>
              <div class="card__content--services">web design, strategy</div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- CTA -->
    <section class="cta">
      <div class="cta__wrapper container">
        <h3 class="cta__text">some text about getting in touch</h3>
        <a href="#" class="gradient-btn">contact button</a>
      </div>
    </section>
  </div>
</template>

<script>
// import VerticalSlider from "./../components/VerticalSlider";

export default {
  components: {
    // VerticalSlider,
  },
};
</script>

<style lang="scss" scoped>
.hero {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: calc(100vh - 200px);

  &__title {
    color: #f8f8f8;
    font-family: "Poppins", sans-serif;
    font-size: 48px;
    line-height: 72px;
    font-weight: 500;
  }

  &__desc {
    color: #f8f8f8;
    font-family: "Open Sans", sans-serif;
    font-size: 16px;
    line-height: 1.5;
    max-width: 50%;
    margin: 16px 0 48px;
  }
}

.showcase {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;

  &__pic {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 80%;
    height: 600px;
    margin-left: auto;
    // background: linear-gradient(90deg, #5096ff, #3bffa4);
    // background: linear-gradient(90deg, #369aff, #ff658a);
    background: linear-gradient(90deg, #ff658a, #369aff);
    background-size: 400% 400%;
    animation: gradient 15s linear infinite;

    @-webkit-keyframes gradient {
      0% {
        background-position: 0% 51%;
      }
      50% {
        background-position: 100% 50%;
      }
      100% {
        background-position: 0% 51%;
      }
    }
    @keyframes gradient {
      0% {
        background-position: 0% 51%;
      }
      50% {
        background-position: 100% 50%;
      }
      100% {
        background-position: 0% 51%;
      }
    }

    img {
      max-height: 70%;
      max-width: 100%;
    }
  }
}

.about-me {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  margin-top: 200px;

  &__text {
    color: #f8f8f8;
    font-family: "Open Sans", sans-serif;
    font-size: 24px;
    line-height: 48px;
    margin-bottom: 48px;
  }
}

.my-work {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  margin-top: 200px;

  &__header {
    display: flex;
    align-items: center;
    justify-content: space-between;

    h1 {
      color: #f8f8f8;
      font-family: "Poppins", sans-serif;
      font-size: 48px;
      line-height: 72px;
      font-weight: 500;
    }
  }

  &__grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 32px;
    width: 100%;
    margin-top: 72px;

    .card {
      display: flex;
      flex-direction: column;

      &__img {
        height: 240px;
        width: 100%;
        background: linear-gradient(90deg, #369aff, #ff658a);
        background-size: cover;
        transition: all 0.2s ease-out;

        &:hover {
          transform: scale(0.98);
        }

        a {
          display: flex;
          align-items: center;
          justify-content: center;
          height: 100%;
          width: 100%;

          img {
            height: 85%;
            transition: all 0.2s ease-out;
            transform-origin: center;
          }

          &:hover img {
            transform: scale(1.1);
          }
        }
      }

      &__content {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: center;
        padding: 16px 0;

        &--title {
          color: #f8f8f8;
          font-family: "Open Sans", sans-serif;
          font-size: 18px;
          line-height: 32px;
        }

        &--services {
          color: rgba(255, 255, 255, 0.7);
          font-family: "Open Sans", sans-serif;
          font-size: 12px;
          line-height: 18px;
        }
      }
    }
  }
}

.cta {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  margin: 200px 0;

  &__wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }

  &__text {
    color: #f8f8f8;
    font-family: "Open Sans", sans-serif;
    font-size: 32px;
    font-weight: 500;
    line-height: 55px;
    margin-bottom: 32px;
  }
}

// MEDIA QUERIES
@media (max-width: 576px) {
  .hero {
    text-align: center;

    &__title {
      font-size: 32px;
      line-height: 48px;
      font-weight: 500;
    }

    &__desc {
      max-width: 100%;
      line-height: 1.5;
    }
  }

  .showcase {
    &__pic {
      height: 400px;
      width: 100vw;

      img {
        height: 90%;
      }
    }
  }

  .about-me {
    margin-top: 48px;

    &__text {
      font-size: 20px;
      line-height: 32px;
      margin-bottom: 32px;
    }
  }

  .my-work {
    margin-top: 150px;

    &__grid {
      grid-template-columns: repeat(1, 1fr);
      margin-top: 48px;
    }
  }

  .cta {
    margin-top: 150px;
    text-align: center;

    &__text {
      font-size: 24px;
      line-height: 32px;
    }
  }
}

@media (min-width: 577px) and (max-width: 1199px) {
  .hero {
    text-align: center;

    &__title {
      font-size: 32px;
      line-height: 48px;
      font-weight: 500;
    }

    &__desc {
      max-width: 100%;
      line-height: 1.5;
    }
  }

  .showcase {
    &__pic {
      height: 400px;
      width: 80%;

      img {
        height: 100%;
      }
    }
  }

  .about-me {
    margin-top: 48px;

    &__text {
      font-size: 20px;
      line-height: 32px;
      margin-bottom: 32px;
    }
  }

  .my-work {
    margin-top: 150px;

    &__grid {
      grid-template-columns: repeat(2, 1fr);
      margin-top: 48px;
    }
  }

  .cta {
    text-align: center;

    &__text {
      font-size: 24px;
      line-height: 32px;
    }
  }
}
</style>
