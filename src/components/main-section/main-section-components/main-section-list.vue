<template>
  <div class="main-section-headers">Personal Information</div>
  <ul class="main-section-list">
    <li
      v-for="info in personal_info_categories"
      :key="info.description"
      class="main-section-item"
    >
      <div class="main-section-information-left">
        <div class="main-section-information-category">
          <div>
            <component :is="info.icon" />
          </div>
          <div class="main-section-information-content">
            {{ info.description }}
          </div>
        </div>
        <div class="main-section-information-item-info">
          {{ info.info }}
        </div>
      </div>
      <div><GenericIcon /></div>
    </li>
  </ul>
</template>

<script>
import GenderIcon from "@/assets/main-section/main-section-personal-Icons/GenderIcon.vue";
import AgeIcon from "@/assets/main-section/main-section-personal-Icons/AgeIcon.vue";
import BirthdayIcon from "@/assets/main-section/main-section-personal-Icons/BirthdayIcon.vue";
import EmailIcon from "@/assets/main-section/main-section-personal-Icons/EmailIcon.vue";
import PhoneIcon from "@/assets/main-section/main-section-personal-Icons/PhoneIcon.vue";
import WhatsappIcon from "@/assets/main-section/main-section-personal-Icons/Whatsapp.vue";
import NationalityIcon from "@/assets/main-section/main-section-personal-Icons/NationalityIcon.vue";
import LocationIcon from "@/assets/main-section/main-section-personal-Icons/LocationIcon.vue";
import GenericIcon from "@/assets/main-section/main-section-personal-Icons/GenericIcon.vue";

export default {
  name: "mainSectionList",
  components: {
    GenericIcon,
  },
  data() {
    return {
      personal_info: {
        gender: "Female",
        age: 28,
        birthDay: "25/08/1994",
        Email: "jessicalewis@jesiccalewis.com",
        Phone: "+971 53837234",
        Whatsapp: "+971 53837234",
        Nationality: "USA",
        Location: "Business Bay, Dubai - UAE ",
      },
      personal_info_categories: [
        { icon: GenderIcon, description: "Gender", info: "Female" },
        { icon: AgeIcon, description: "Age", info: 28 },
        {
          icon: BirthdayIcon,
          description: "Date of Birth",
          info: "25/08/1994",
        },
        {
          icon: EmailIcon,
          description: "Email",
          info: "jessicalewis@jesiccalewis.com",
        },
        { icon: PhoneIcon, description: "Phone", info: "+971 53837234" },
        { icon: WhatsappIcon, description: "Whatsapp", info: "+971 53837234" },
        { icon: NationalityIcon, description: "Nationality", info: "USA" },
        {
          icon: LocationIcon,
          description: "Location",
          info: "Business Bay, Dubai - UAE",
        },
      ],
    };
  },
};
</script>

<style>
.main-section-personal-information {
  background-color: #ffffff;

  /* min-width: 300px;*/
  width: 40%;
  border-radius: 7px;
  /*padding-bottom: 10px;*/
}
</style>
