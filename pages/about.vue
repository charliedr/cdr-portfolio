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
    <!-- EXPERIENCE -->
    <div class="about__experience">
      <div class="container">
        <div class="about__experience--left">
          <h2 class="about__experience--title">
            experience
          </h2>
        </div>
        <div class="about__experience--right">
          <p class="about__experience--desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed unde sint nesciunt numquam consequatur, similique esse facere obcaecati cupiditate excepturi?</p>
          <p class="about__experience--desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed unde sint nesciunt numquam consequatur, similique esse facere obcaecati cupiditate excepturi?</p>
        </div>
      </div>  
    </div> 
    <!-- skills -->
    <div class="about__skills">
      <div class="container">
        <div class="about__skills--left">
          <h2 class="about__skills--title">
            skills
          </h2>
        </div>
        <div class="about__skills--right">
          <div>
            <ul class='skills__list'>
              <li class='skills__list--item'>HTML</li>
              <li class='skills__list--item'>CSS</li>
              <li class='skills__list--item'>SASS</li>
              <li class='skills__list--item'>JavaScript</li>
              <li class='skills__list--item'>Vue.js</li>
              <li class='skills__list--item'>Nuxt.js</li>
              <li class='skills__list--item'>Node.js</li>
            </ul>
          </div>
          <div>
            <ul class='skills__list'>
              <li class='skills__list--item'>Web Design</li>
              <li class='skills__list--item'>UI/UX Design</li>
              <li class='skills__list--item'>Search Engine Optimization (SEO)</li>
              <li class='skills__list--item'>Website Accessibility</li>
              <li class='skills__list--item'>Adobe XD</li>
              <li class='skills__list--item'>Adobe Photoshop</li>
              <li class='skills__list--item'>Adobe Premiere</li>
            </ul>
          </div>
        </div>
      </div>  
    </div> 
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

.about__experience {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  padding-bottom: 64px;

  > .container {
    border-top: 1px solid #f8f8f8;
    display: flex;
    flex-direction: row;
  }

  &--left, &--right {
    width: 50%;
    padding-top: 24px;
    // outline: 1px solid red;
  }

  &--title {
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    color: #f8f8f8;
    font-weight: 400;
    text-transform: uppercase;
  }

  &--desc {
    color: #f8f8f8;
    font-family: "Open Sans", sans-serif;
    font-size: 16px;
    line-height: 1.5;
    padding-bottom: 16px;
  }
}

.about__skills {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  padding-bottom: 64px;

  > .container {
    border-top: 1px solid #f8f8f8;
    display: flex;
    flex-direction: row;
  }

  &--left, &--right {
    width: 50%;
    padding-top: 24px;
  }

  &--right {
    display: flex;
    flex-direction: row;
    justify-content: space-between
  }

  &--title {
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    color: #f8f8f8;
    font-weight: 400;
    text-transform: uppercase;
  }

  .skills__list {
    list-style-type: none;
    padding: 0;

    &--item {
      color: #f8f8f8;
      font-family: "Open Sans", sans-serif;
      font-size: 16px;
      line-height: 1.75;
    }
  }
}

.about__clients {
  display: flex;
  // align-items: flex-start;
  justify-content: center;
  width: 100%;
  margin: 200px 0;

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
    margin: 150px 0;
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
    margin-bottom: 150px;
    
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
