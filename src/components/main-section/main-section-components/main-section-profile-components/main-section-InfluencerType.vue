<template>
  <div class="main-section-influencer-type-list">
    <div
      v-for="(type, index) in influencerTypes"
      :key="index"
      class="main-section-influencer-type-element"
    >
      {{ type }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      influencerTypes: ["Lifestyle", "Travel", "Food & Beverages"], // Your list of influencer types
    };
  },
};
</script>

<style scoped>
.main-section-influencer-type-list {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 10px; /* Gap between grid items */
}

.main-section-influencer-type-element {
  padding: 5px 15px;
  background-color: #00a4b6;
  border-radius: 5px;
  color: white;
}
</style>
