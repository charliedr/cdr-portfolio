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
          <img src="@/assets/iphone.png" alt="iPhone mockup" />
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
        <a href="#" class="link">link to about page</a>
      </div>
    </section>
    <!-- WORK -->
    <section class="my-work">
      <div class="container">
        <div class="my-work__header">
          <h1 class="my-work__title">work</h1>
          <a href="#" class="link">link to work page</a>
        </div>
        <div class="my-work__grid">
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
export default {};
</script>

<style lang="scss" scoped>
.hero {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: calc(100vh - 200px);

  &__title {
    color: #fff;
    font-family: "Poppins", sans-serif;
    font-size: 48px;
    line-height: 72px;
    font-weight: 500;
  }

  &__desc {
    color: #fff;
    font-family: "Open Sans", sans-serif;
    font-size: 16px;
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
    display: flex;
    align-items: center;
    justify-content: center;
    width: 80%;
    height: 600px;
    background: linear-gradient(90deg, #5096ff, #3bffa4);
    margin-left: auto;

    img {
      height: 70%;
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
    color: #fff;
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
      color: #fff;
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
        background: linear-gradient(90deg, #5096ff, #3bffa4);
        background-size: cover;

        a {
          display: flex;
          align-items: center;
          justify-content: center;
          height: 100%;
          width: 100%;

          img {
            height: 85%;
            transition: all 0.2s ease-in-out;
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
        padding: 24px 0;

        &--title {
          color: #fff;
          font-family: "Open Sans", sans-serif;
          font-size: 20px;
          line-height: 24px;
        }

        &--services {
          color: rgba(255, 255, 255, 0.7);
          font-family: "Open Sans", sans-serif;
          font-size: 16px;
          line-height: 24px;
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
  margin-top: 200px;

  &__wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }

  &__text {
    color: #fff;
    font-family: "Open Sans", sans-serif;
    font-size: 32px;
    font-weight: 500;
    line-height: 55px;
    margin-bottom: 32px;
  }
}
</style>
