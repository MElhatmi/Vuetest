<template>
  <topSection @active-tab-changed="handleActiveTabChanged" />
  <template v-if="activeTabIndex === 0">
    <mainSection :activeTabIndex="activeTabIndex" />
  </template>
  <template v-else-if="activeTabIndex === 1">
    <div></div>
  </template>
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
  data() {
    return {
      activeTabIndex: 0, // Initialize activeTabIndex in the parent component
    };
  },
  methods: {
    handleActiveTabChanged(newTabIndex) {
      // Update the activeTabIndex when receiving the event from TopSection
      this.activeTabIndex = newTabIndex;
    },
  },
};
</script>

<style>
.emptyspace {
  flex: 0 20; /* Adjust as needed */
  /* max-width: 20%; Adjust as needed */
}
</style>
