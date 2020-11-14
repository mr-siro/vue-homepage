<template>
  <div class="why-should-wrapper">
    <b-container>
      <div class="main-text-why">
        <h3 class="why-title">{{txt.whyTitle}}</h3>
        <p class="why-sub">{{txt.whySub}}</p>
      </div>
      <div class="main-list-why">
        <div v-for="item in listWhy" :key="item.id">
          <CateFeature
          :image="item.img"
          :title="item.title"
          :description="item.description"
          :container-style="{flexDirection:'column', alignItems:'center'}"
          :text-float="'center'"
          :img-style="{marginBottom:'2rem'}"
          :content-style="{marginBottom: '3rem'}"
          />
        </div>
      </div>
    </b-container>
  </div>
</template>

<script>
import {listWhy} from "@/shared/dummy";
import CateFeature from "@/components/card/CateFeature";
export default {
  name: "WhyShould",
  data() {
    return {
      txt: {
        whyTitle: 'Why you should choose our app',
        whySub: "The rise of mobile devices transforms the way we consume information entirely and the world's most elevant channels such as Facebook."
      },
      listWhy:listWhy
    }
  },
  components:{
    CateFeature
  }
}
</script>

<style scoped>
.why-should-wrapper {
  padding-top: 6rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.why-title {
  color: #242f51;
  font-weight: bold;
}
.why-sub {
  color: #616368;
}

.main-text-why {
  max-width: 640px;
  display: inline-block;
}

.main-list-why {
  display: flex;
  flex-wrap: wrap;
  margin: 5rem;
  align-items: center;
  justify-content: space-between;
}

</style>
