<template>
  <div class="home-wrapper">
    <div class="home-header">
      <Header/>
    </div>
    <div class="home-content">
      <Trusted/>
      <Features/>
      <SmartJackPot/>
      <Designed/>
      <WhyShould/>
      <UltimateFeatures/>
      <GetAwesome/>
      <Testimonial/>
      <Faq/>
      <StartFree/>
    </div>
    <div class="home-footer">
      <Footer/>
    </div>
    <BackToTop title="Top"/>
  </div>
</template>

<script>
import Header from "@/pages/homepage/Header/Header";
import Footer from "@/pages/homepage/Footer/Footer";
import Trusted from "@/pages/homepage/Content/Trusted/Trusted";
import Features from "@/pages/homepage/Content/Features/Features";
import SmartJackPot from "@/pages/homepage/Content/Smartjackpot/SmartJackPot";
import Designed from "@/pages/homepage/Content/Designed/Designed";
import WhyShould from "@/pages/homepage/Content/Whyshould/WhyShould";
import UltimateFeatures from "@/pages/homepage/Content/UltimateFeatures/UltimateFeatures";
import GetAwesome from "@/pages/homepage/Content/Getawesome/GetAwesome";
import Testimonial from "@/pages/homepage/Content/Testimonial/Testimonial";
import Faq from "@/pages/homepage/Content/FAQ/Faq";
import StartFree from "@/pages/homepage/Content/Startfree/StartFree";
import BackToTop from "@/components/button/BackToTop";
export default {
  name: 'Home',
  components: {
    Header,
    Footer,
    Trusted,
    Features,
    SmartJackPot,
    Designed,
    WhyShould,
    GetAwesome,
    Testimonial,
    Faq,
    StartFree,
    UltimateFeatures,
    BackToTop
  }
}
</script>
<style>
.home-wrapper {
  display: grid;
  grid-template-columns: 3fr;
}
.home-header, .home-content, .home-footer {
  grid-column: 1/3;
  width: 100%;
}
</style>
