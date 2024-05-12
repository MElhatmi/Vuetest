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
      <div class="main-section-socialHandle-description">
        {{ social.description }}
      </div>
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
  margin: 0 auto;
  /*padding: 0 calc(15px + 1vw) 20px calc(15px + 1vw);*/
  display: grid;
  grid-template-columns: repeat(
    auto-fill,
    minmax(80px, 1fr)
  ); /* Adjust as needed */ /* Start from the left */
  gap: calc(10px + 0.5vw);
  width: 85%;
  padding-bottom: 30px;
}
.main-section-socialHandle {
  text-align: center;
  font-size: 13px;
  color: #777777;
}
/*.main-section-socialHandles-wrapper {
  padding: 0 calc(15px + 1vw) 20px calc(15px + 1vw);
}*/
</style>
