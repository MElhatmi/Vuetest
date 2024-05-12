<template>
  <div class="main-section-container">
    <div class="emptyspace"></div>
    <main class="main-section">
      <section class="main-section-personal-information">
        <mainSectionList />
      </section>
      <section class="main-section-profileAndSocial-information">
        <section class="main-section-profile-Info">
          <mainProfile />
        </section>
        <section class="main-section-social-handles"><socialHandles /></section>
      </section>
    </main>
    <div class="emptyspace"></div>
  </div>
</template>

<script>
import mainSectionList from "./main-section-components/main-section-list.vue";
import mainProfile from "./main-section-components/main-section-profile.vue";
import socialHandles from "./main-section-components/main-section-socialHandles.vue";
export default {
  name: "mainSection",
  components: {
    mainSectionList,
    mainProfile,
    socialHandles,
  },
};
</script>

<style>
.active {
  color: #00a4b6;
  border-bottom: solid 0.3rem;
}
.main-section-container {
  /* width: 80%;
  margin: 2rem auto;*/
  margin: 2rem 0;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}
.main-section {
  flex-shrink: 0;
  flex-basis: 60%;
  min-width: min(700px, 90%);
  display: flex;
  gap: 15px;
  margin-bottom: 2rem;
}
.main-section-profileAndSocial-information {
  /* min-width: 375px;*/
  width: 60%;
}
.main-section-social-handles {
  background-color: #ffffff;
  border-radius: 7px;
}
.main-section-headers {
  padding: 18px 26px;
  font-size: 18px;
  font-weight: bold;
  color: #383838;
}
.main-section-item {
  padding: 10px calc(10px + 0.5vw) 10px 26px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.main-section-list li {
  border-top: 1px solid #efefef;
}
.main-section-information-category {
  display: flex;
  align-items: center;
  gap: 10px;
}
.main-section-information-item-info {
  padding-left: 22px;
  padding-top: 5px;
  color: #181818;
  font-size: 16px;
  word-wrap: break-word;
}
.main-section-information-left {
  width: 80%;
}
.main-section-information-content {
  color: #828080;
  font-size: 15px;
}
@media only screen and (max-width: 768px) {
  .main-section {
    flex-wrap: wrap;
    justify-content: center;
    min-width: 90%;
  }
  .main-section-personal-information {
    width: 100%;
  }
  .main-section-profileAndSocial-information {
    min-width: 200px;
    width: 100%;
  }
}
</style>
