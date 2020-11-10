<template>
  <section class="vertical-slider">
    <div class="col-wrapper">
      <div class="col">
        <div class="iphone-mockup-wrapper">
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
        </div>
      </div>
      <div class="col">
        <div class="iphone-mockup-wrapper">
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
        </div>
      </div>
      <div class="col">
        <div class="iphone-mockup-wrapper">
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
          <img
            src="@/assets/iphone-front.png"
            alt="iPhone mockup"
            class="iphone-mockup"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "VerticalSlider",
};
</script>

<style lang="scss" scoped>
.vertical-slider {
  margin-bottom: 200px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.col-wrapper {
  display: flex;
  flex-direction: row;
  width: 100%;
  height: 100%;
  overflow: hidden;

  .col {
    display: flex;
    align-items: baseline;
    width: 33.3%;
    transform: skew(-6deg, -8deg);

    .iphone-mockup-wrapper {
      width: 100%;
      transform: translateY(0);
      animation: 30s 0.5s infinite forwards linear verticalScroll;

      @keyframes verticalScroll {
        from {
          transform: translateY(0);
        }
        to {
          transform: translateY(-100%);
        }
      }

      .iphone-mockup {
        width: 100%;
        transform: scale(2);
        margin-bottom: 100%;
      }
    }
  }
}
</style>
