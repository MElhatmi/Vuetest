<template>
  <div class="main-section-container">
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
.main-section-container {
  display: flex;
  justify-content: center;
  padding: 30px calc(50px + 15vw) 30px calc(50px + 15vw);
}
.main-section {
  display: flex;
  gap: calc(10px + 2vw);
}
.main-section-profileAndSocial-information {
  min-width: 200px;
  width: calc(220px + 23vw);
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
  padding: 10px 32px 10px 40px;
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
  padding-left: 25px;
  padding-top: 5px;
  color: #181818;
  font-size: 16px;
  word-wrap: break-word;
}
.main-section-information-left {
  width: 100%;
}
.main-section-information-content {
  color: #828080;
  font-size: 15px;
}
@media only screen and (max-width: 768px) {
  .main-section {
    flex-wrap: wrap;
    justify-content: center;
  }
  .main-section-personal-information {
    width: 100%;
  }
  .main-section-profileAndSocial-information {
    min-width: 200px;
    width: 100%;
  }
  .main-section-container {
    padding-right: calc(15px + 1vw);
    padding-left: calc(15px + 1vw);
  }
}
</style>
