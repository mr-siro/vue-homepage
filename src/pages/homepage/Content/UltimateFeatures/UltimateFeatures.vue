<template>
  <div class="ultimate-features-wrapper">
    <div class="container-lg">
    <b-row class="d-flex align-items-center">
      <div class="col-md-7">
        <div class="left-ultimate">
          <h3 class="ut-title">{{txt.ultimateTitle}}</h3>
          <p class="ut-sub my-3">{{txt.ultimateSub}}</p>

          <div class="main-list-ultimate">
            <div v-for="item in listUltimate" :key="item.id">
              <CateFeature
              :image="item.img"
              :title="item.title"
              :description="item.description"
              :container-style="{flexDirection:'column', alignItems:'left'}"
              :img-style="{marginBottom:'2rem'}"
              :content-style="{marginBottom: '1.5rem'}"
              />
            </div>
          </div>
          <b-button class="btn-try" pill variant="primary">See all</b-button>
        </div>
      </div>
      <div class="col-md-5">
        <div class="right-ultimate">
          <img style="max-width: 100%" alt="#" :src="images.phone3">
        </div>
      </div>
    </b-row>
    </div>
  </div>
</template>

<script>
import {Images} from "@/assets/Images";
import {listUltimate} from "@/shared/dummy";
import CateFeature from "@/components/card/CateFeature";
export default {
  name: "UltimateFeatures",
  data() {
    return {
      images: {
        phone3: Images.phone3
      },
      txt:{
        ultimateTitle:'Ultimate features that we built',
        ultimateSub:"The rise of mobile devices transforms the way we consume information entirely."
      },
      listUltimate:listUltimate
    }
  },
  components:{
    CateFeature
  }
}
</script>

<style scoped>
.ultimate-features-wrapper {
  background-image: url("../../../../assets/images/background-ulti.png");
  background-position: right center;
  background-repeat: no-repeat;
  background-size: initial;
}

.ut-title {
  color: #242f51;
  font-weight: bold;
  max-width: 320px;
}
.ut-sub {
  color: #616368;
  max-width: 390px;
}

.left-ultimate {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  text-align: left;
}
.main-list-ultimate {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 2rem;
}
.btn-try {
  background-color: #2500f9;
}
</style>
