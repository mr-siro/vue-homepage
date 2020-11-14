<template>
  <div class="smart-jackpot-wrapper pt-3">
    <b-container>
      <b-row>
        <div class="col-md-6" style="border-right: 0.5px solid darkgrey">
          <h2 class="jackpot-title">{{txt.JackpotTitle}}</h2>
        </div>
        <div class="col-md-6">
          <p class="jackpot-des">{{txt.JackpotDes}}</p>
        </div>
      </b-row>
      <div class="lst-wrapper">
        <div v-for="item in listSmartJackpot" :key="item.id">
          <CateFeature
              class="jackpot-item"
              :container-style="{flexDirection:'column', alignItems:'flex-start'}"
              :img-style="{marginBottom:'2rem'}"
              :title-color="item.color"
              :title="item.title"
              :description="item.description"
              :image="item.img"/>
        </div>
      </div>

    </b-container>
  </div>
</template>

<script>
import {listSmartJackpot} from "@/shared/dummy";
import CateFeature from "@/components/card/CateFeature";

export default {
  name: "SmartJackPot",
  data() {
    return {
      txt: {
        JackpotTitle: 'Smart jackpots that you may love this anytime & anywhere',
        JackpotDes: "The rise of mobile devices transforms the way we consume information entirely and the world's most elevant channels such as Facebook."
      },
      listSmartJackpot: listSmartJackpot
    }
  },
  components: {
    CateFeature
  }
}
</script>

<style scoped>
.jackpot-des {
  color: #616368;
  text-align: left;
  max-width: 400px;
}

.jackpot-title {
  color: #242f51;
  text-align: left;
  font-weight: 800;
  max-width: 400px;
}

.lst-wrapper {
  display: flex;
  padding: 10% 0;
  flex-wrap: wrap;
  align-items: flex-start;
  justify-content: flex-start;
}

.jackpot-item {
  margin-right: 5rem;
}
</style>
