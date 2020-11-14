<template>
<div class="start-free-wrapper">
  <b-container>
    <div class="main-start">
      <h2>Download our App now !</h2>
      <p class="py-2">{{txt.sub}}</p>
      <div class="view-download">
        <img class="img-start mx-2" alt="#" :src="images.chPlay">
        <img class="img-start ml-2" alt="#" :src="images.appStore">
      </div>
    </div>
  </b-container>
</div>
</template>

<script>
import {Images} from "@/assets/Images";

export default {
name: "StartFree",
  data() {
  return {
    txt:{
      sub:"The rise of mobile devices transforms the way we consume information entirely and the world's most elevant channels such as Facebook."
    },
    images:{
      chPlay: Images.chPlay,
      appStore: Images.appStore
    }
  }
  }
}
</script>

<style scoped>
.start-free-wrapper {
  background-image: url("../../../../assets/images/bg_start_03.png");
  background-position: right bottom;
  background-repeat: no-repeat;
  background-size: initial;
  padding-top: 10%;
  border-top: 0.5px solid lightgray;
  min-height: 100vh;
}

h2 {
  color: #242f51;
  font-weight: bold;
  text-align: left;
}
p {
  color: #616368;
  text-align: left;
}

.main-start {
  display: flex;
  justify-content: flex-start;
  flex-direction: column;
  align-items: flex-start;
  max-width: 600px;
}
.img-start {
  max-width: 120px;
}
</style>
