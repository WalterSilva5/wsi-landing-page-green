<template>
  <div style="margin: 0; padding: 0"><page /></div>
</template>

<script>
import Page from "./components/Page.vue";
export default {
  components: {
    Page,
  },
};
</script>

<style lang="scss">
body {

  background-image: linear-gradient(
    to bottom right,
    rgba(193, 255, 231, 0.300),
    rgba(0, 255, 34, 0.3)
  );
  background-repeat: no-repeat;
  min-height: 100vh;
}
</style>
