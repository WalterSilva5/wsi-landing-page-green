<template>
  <div>
    <nav
      class="
        mt-5 mt-auto
        navbar navbar-expand navbar-dark
        footer
        d-flex
        justify-content-center
      "
    >
      <a href="https://waltersilva5.github.io/">
        <h4 class="text-secondary text-center">
          @waltersilva5
          <small style="font-size: 13px; vertical-align: text-top">®</small> -
          <span>{{ new Date().getFullYear() }}.</span>
        </h4></a
      >
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: rgb(0, 46, 31);
}
a{text-decoration: none;}
</style>
