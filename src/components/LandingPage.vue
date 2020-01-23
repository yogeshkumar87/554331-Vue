<template>
<div>
  <ReviewPage />
</div>
</template>

<script>
import ReviewPage from "./ReviewPage.vue";
export default {
  name: "LandingPage",
  components: {
    ReviewPage
  },
  data() {
    return {
      welcomeMsg: "Welcome to Mini Good Read",
      appDesc:
        "A sample app developed to serve the purpose of learning Vue at VueFest 2020"
    };
  }
};
</script>
<style>
.landing-wrapper {
  padding: 5rem;
  text-align: center;
}

.landing-wrapper h2 {
  font-size: 7rem;
}

.landing-wrapper .app-description {
  padding: 3rem 0;
  font-size: 2rem;
  text-align: center;
  color: #44576e;
}
</style>
