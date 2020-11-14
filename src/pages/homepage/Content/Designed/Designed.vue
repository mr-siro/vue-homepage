<template>
  <div class="designed-wrapper">
    <b-row class="d-flex align-items-center">
      <div class="col-md-6">
        <div class="left-design">
          <img style="max-width: 100%" alt="#" :src="images.imgDesign">
        </div>

      </div>
      <div class="col-md-6">
        <div class="right-design">
          <h3 class="ds-title">{{txt.designTitle}}</h3>
          <p class="ds-sub my-4">{{txt.designDes}}</p>
          <b-button class="btn-try" pill variant="primary">Learn more</b-button>
        </div>
      </div>
    </b-row>
  </div>
</template>

<script>
import {Images} from "@/assets/Images";

export default {
  name: "Designed",
  data() {
    return {
      images: {
        imgDesign: Images.DesignImg
      },
      txt: {
        designTitle: 'Designed & built by the latest code integration',
        designDes: "The rise of mobile devices transforms the way we consume information entirely and the world's most elevant channels such as Facebook."
      }
    }
  }
}
</script>

<style scoped>
.designed-wrapper {
  margin: 0 2em;
}

.right-design {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  text-align: left;
}
.ds-title {
  color: #242f51;
  font-weight: bold;
  max-width: 360px;
}
.ds-sub {
  color: #616368;
  max-width: 400px;
}

.btn-try {
  background-color: #2500f9;
}
</style>
