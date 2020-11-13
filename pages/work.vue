<template>
  <div>
    <!-- HERO -->
    <section class="work__hero">
      <div class="container">
        <h1 class="work__hero--title">
          <span>work blah blah</span> <span>blah</span>
        </h1>
      </div>
    </section>
    <!-- PORTFOLIO GRID -->
    <section class="portfolio">
      <div class="container">
        <div class="portfolio__wrapper">
          <NuxtLink :to="item.link" v-for="item in portfolio" :key="item.title" :style="{ backgroundImage: `url('${item.image}')` }" class="portfolio__item">
            <h1 class="portfolio__item--title" v-html="item.title"></h1>
          </NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      portfolio: [
        // { title: 'AXIOM Architecture', link: '/', image: '_nuxt/assets/AXIOM-thumbnail.jpg'},
        { title: 'AXIOM Architecture', link: '/', image: '@/assets/AXIOM-thumbnail.jpg'},
        { title: 'DJ Johnson For State Rep', link: '/', image: '@/assets/DJ-thumbnail.jpg'},
        { title: 'Phoebe For Mayor', link: '/', image: '@/assets/AXIOM-thumbnail.jpg'},
      ]
    }
  }
};
</script>

<style lang="scss" scoped>
.work__hero {
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
    
    &::before {
      content: "";
      width: 100px;
      height: 2px;
      position: absolute;
      left: 0px;
      bottom: -24px;
      background: linear-gradient(90deg, #ff658a, #369aff);
    }
  }
}

.portfolio {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  margin: 200px 0;

  &__wrapper {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: masonry;
    gap: 24px;

    a {
      text-decoration: none;
    }
  }

  &__item {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    min-height: 300px;
    padding: 24px;
    background-size: cover;
    transition: all .2s ease-in-out;

    &::after {
      content: '';
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      // background: rgba(0, 0, 0, 0);
      background: linear-gradient(90deg, #ff658a, #369aff);
      opacity: 0;
      transition: all .2s ease-in-out;
    }

    &:hover::after {
      // background: rgba(0, 0, 0, 0.85);
      background: linear-gradient(90deg, #ff658a, #369aff);
      opacity: 65%;
    }

    &--title {
      display: inline-block;
      font-family: "Poppins", sans-serif;
      font-weight: 600;
      text-align: center;
      color: #fff;
      z-index: 5;
      opacity: 0;
    }

    &:hover .portfolio__item--title{
      opacity: 1;
    }
  }
}

// MEDIA QUERIES
@media (max-width: 576px) {
  .work__hero {
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
}

@media (min-width: 577px) and (max-width: 1199px) {
  .work__hero {
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
}
</style>
