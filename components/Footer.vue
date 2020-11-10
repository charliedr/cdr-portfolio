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
  background-color: #0d0d0d;
  display: flex;
  justify-content: center;
  padding: 24px;

  div {
    display: flex;
    align-items: center;
    justify-content: center;

    .copyright {
      color: rgba(248, 248, 248, 0.7);
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
