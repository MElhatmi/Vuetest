<template>
  <topSection />
  <mainSection />
</template>

<script>
import mainSection from "./components/main-section/main-section.vue";
import topSection from "./components/top-section/top-section.vue";
export default {
  name: "App",
  components: {
    topSection,
    mainSection,
  },
};
</script>

<style>
#app {
  font-family: Greycliff CF, sans-serif;
  height: 100%;
}
</style>
