<template>
  <div class="main-section-headers">Social Handles</div>
  <div class="main-section-socialHandles">
    <div
      class="main-section-socialHandle"
      v-for="social in socialHandles"
      :key="social.description"
    >
      <div>
        <component :is="social.icon" />
      </div>
      <div>{{ social.description }}</div>
    </div>
  </div>
</template>
<script>
import InstagramSocialHandle from "@/assets/main-section/main-section-socialHandles-Icons/Instagram-socialHandle-Icon.vue";
import TikTokSocialHandle from "@/assets/main-section/main-section-socialHandles-Icons/TikTok-socialHandle-Icon.vue";
import SnapchatSocialHandle from "@/assets/main-section/main-section-socialHandles-Icons/Snapchat-socialHandle-Icon.vue";
import TwitchSocialHandle from "@/assets/main-section/main-section-socialHandles-Icons/Twitch-socialHandle-Icon.vue";
import YoutubeSocialHandle from "@/assets/main-section/main-section-socialHandles-Icons/Youtube-socialHandle-Icon.vue";

export default {
  name: "socialHandles",
  data() {
    return {
      socialHandles: [
        {
          icon: InstagramSocialHandle,
          description: "jessicalewis",
        },
        {
          icon: TikTokSocialHandle,
          description: "jessicalewis",
        },
        {
          icon: SnapchatSocialHandle,
          description: "Snapchat",
        },
        {
          icon: TwitchSocialHandle,
          description: "Twitch",
        },
        {
          icon: YoutubeSocialHandle,
          description: "Youtube",
        },
      ],
    };
  },
};
</script>

<style>
.main-section-socialHandles {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  padding: 0 calc(10px + 0.5vw) 20px calc(10px + 0.5vw);
  gap: calc(10px + 0.5vw);
}
.main-section-socialHandle {
  text-align: center;
  font-size: 13px;
  color: #777777;
}
</style>
