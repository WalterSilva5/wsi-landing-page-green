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
    rgb(108, 255, 199),
    rgb(1, 110, 105)
  );
  background-repeat: no-repeat;
  min-height: 100vh;
}
</style>
