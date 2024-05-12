<template>
  <div class="progress-bar-container">
    <div class="progress-bar">
      <div class="progress" :style="{ width: progress + '%' }"></div>
    </div>
    <div class="progress-label">{{ progress }}%</div>
  </div>
</template>

<script>
export default {
  name: "profileCompletionBar",
  props: {
    progress: {
      type: Number,
      required: true,
      validator: (value) => value >= 0 && value <= 100,
    },
  },
};
</script>

<style scoped>
.progress-bar {
  width: 100%;
  height: 15px;
  background-color: #f0f0f0;
  border-radius: 25px;
  overflow: hidden;
}

.progress {
  height: 100%;
  background-color: #00a4b6;
  border-radius: 0 25px 25px 0;
}
.progress-bar-container {
  display: flex;
  align-items: center;
  gap: 20px;
}

.progress-label {
  font-size: 15px;
  color: #181818;
}
</style>
