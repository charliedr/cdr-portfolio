<template>
  <section class="footer">
    <div class="container">
      <div class="copyright">
        &copy;{{ new Date().getFullYear() }}
        copyright stuff
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
.footer {
  background-color: #121212;
  display: flex;
  justify-content: center;
  padding: 24px;
  margin-top: 200px;

  div {
    display: flex;
    align-items: center;
    justify-content: center;

    .copyright {
      color: rgba(255, 255, 255, 0.7);
      font-family: "Poppins", sans-serif;
      font-size: 16px;
      font-weight: 400;
      line-height: 24px;
    }
  }
}

@media (max-width: 576px) {
  .footer {
    margin-top: 150px;
  }
}
</style>
