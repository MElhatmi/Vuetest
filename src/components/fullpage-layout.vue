<template>
  <topSection />
  <mainSection />
</template>

<script>
import mainSection from "./main-section/main-section.vue";
import topSection from "./top-section/top-section.vue";
export default {
  name: "fullpageLayout",
  components: {
    topSection,
    mainSection,
  },
};
</script>

<style>
.emptyspace {
  flex: 0 20; /* Adjust as needed */
  /* max-width: 20%; Adjust as needed */
}
</style>
