<template>
  <section class="top-section">
    <div class="emptyspace"></div>
    <div class="top-section-container">
      <div class="top-section-profile">
        <profileImage />
        <div class="top-section-profile-info">
          <div class="top-section-profile-name">Jessica Lewis</div>
          <div class="top-section-profile-instagram">
            <topsectionInstagram />
            <div>Jessica Lewis</div>
          </div>
          <div class="top-section-profile-instagram-followers">
            100K - 500K followers
          </div>
        </div>
      </div>
      <ul class="top-section-tabs">
        <li class="top-section-tab-element active">User Details</li>
        <li class="top-section-tab-element">Analytics</li>
      </ul>
    </div>
    <div class="emptyspace"></div>
  </section>
</template>

<script>
import profileImage from "../../assets/top-section/top-sectionImage.vue";
import topsectionInstagram from "../../assets/top-section/top-sectionInstagram.vue";
export default {
  name: "topSection",
  components: {
    profileImage,
    topsectionInstagram,
  },
};
</script>

<style>
.top-section-container {
  margin-top: 2rem;
  flex-shrink: 0;
  flex-basis: 60%;
  min-width: min(700px, 90%);
  /*padding-top: 60px;
  width: 80%;
  margin: auto;*/
}
.top-section {
  /*height: 25%;*/
  /*padding: calc(20px + 3vh) calc(50px + 15vw) 0 calc(50px + 15vw);*/
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  background-color: #fdfdfd;
}
.top-section-profile {
  display: flex;
  padding-bottom: 50px;
}
.top-section-profile-info {
  padding: 8px calc(30px + 1vw);
}
.top-section-profile-name {
  color: #383838;
  font-size: 30px;
  font-weight: 600;
  padding: 5px 0;
}
.top-section-profile-instagram {
  display: flex;
  font-size: 18px;
  color: #606060;
  gap: 10px;
  padding-bottom: 20px;
}
.top-section-profile-instagram-followers {
  color: #383838;
  font-size: 22px;
}
.top-section-tabs {
  display: flex;
  gap: calc(55px + 0.25vw);
  font-size: 18px;
}
.top-section-tabs li {
  display: inline-block;
  position: relative;
  padding-bottom: 22px;
}
/*.top-section-tabs li:hover {
  color: #00a4b6;
}*/
.top-section-tabs li .active {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: #00a4b6;
  height: 4px;
  border-radius: 10px;
}
/*
.top-section-tabs li:hover {
  outline: 4px solid #00a4b6;
  color: #00a4b6;
}*/
@media only screen and (max-width: 768px) {
  .top-section-profile {
    display: block;
  }
  .top-section-profile-info {
    padding-left: 0;
  }
  /*.top-section {
    padding-right: calc(15px + 1vw);
    padding-left: calc(15px + 1vw);
  }*/
  .top-section {
    background-image: linear-gradient(to bottom, #caeaee 30%, transparent 30%);
  }

  .top-section-container {
    min-width: 90%;
  }
}
</style>
