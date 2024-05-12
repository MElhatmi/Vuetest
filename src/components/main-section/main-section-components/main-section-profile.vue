<template>
  <div class="main-section-headers">Profile Information</div>
  <ul class="main-section-list">
    <li class="main-section-item plus-padding">
      <div class="main-section-information-left-profile">
        <div class="main-section-information-category">
          <SignupIcon />
          <div class="main-section-information-content">Sign up date</div>
        </div>
        <div class="main-section-information-item-info">23/04/2023</div>
      </div>
    </li>
    <li class="main-section-item">
      <div class="main-section-information-left-profile">
        <div class="main-section-information-category">
          <ProfileCompletionIcon />
          <div class="main-section-information-content">Profile Completion</div>
        </div>
        <div class="main-section-information-item-info-nontextual">
          <profileCompletionBar :progress="50" />
        </div>
      </div>
    </li>
    <li class="main-section-item">
      <div class="main-section-information-left-profile">
        <div class="main-section-information-category">
          <InfluencerTypeIcon />
          <div class="main-section-information-content">Influencer Type</div>
        </div>
        <div class="main-section-information-item-info-nontextual">
          <InfluencerTypeList />
        </div>
      </div>
    </li>
    <li class="main-section-item">
      <div class="main-section-information-left-profile bottom-padding">
        <div class="main-section-information-category">
          <InfluencerCategoryIcon />
          <div class="main-section-information-content">
            Influencer Category
          </div>
        </div>
        <div class="main-section-information-item-info">Instagram Verified</div>
      </div>
    </li>
  </ul>
</template>

<script>
import InfluencerTypeIcon from "@/assets/main-section/main-section-profile-Icons/InfluencerTypeIcon.vue";
import InfluencerCategoryIcon from "@/assets/main-section/main-section-profile-Icons/InfluencerCategoryIcon.vue";
import InfluencerTypeList from "./main-section-profile-components/main-section-InfluencerType.vue";
import profileCompletionBar from "./main-section-profile-components/main-section-profileCompletion.vue";
import ProfileCompletionIcon from "@/assets/main-section/main-section-profile-Icons/ProfileCompletionIcon.vue";
import SignupIcon from "@/assets/main-section/main-section-profile-Icons/SignupIcon.vue";

export default {
  name: "mainProfile",
  components: {
    SignupIcon,
    ProfileCompletionIcon,
    profileCompletionBar,
    InfluencerTypeIcon,
    InfluencerTypeList,
    InfluencerCategoryIcon,
  },
};
</script>

<style>
.main-section-profile-Info {
  background-color: #ffffff;
  margin-bottom: 15px;
  border-radius: 7px;
}
/*.plus-padding {
  padding-top: 30px;
  padding-bottom: 30px;
}*/
.bottom-padding {
  padding-bottom: 20px;
}
.main-section-information-item-info-nontextual {
  padding-left: 22px;
  padding-top: 10px;
  padding-bottom: 20px;
}
.main-section-information-left-profile {
  width: 100%;
}
</style>
