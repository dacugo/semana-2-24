<template>
  <div>
    <div class="row mt-md-5 mt-sm-5 mt-xs-5">
      <div
        class="col-lg-6 col-xs-6"
        v-for="(newss, index) of news" :key="index">

        <div class="card border-light mb-3" style="max-width: 700px">
          <div class="row no-gutters">
            <div class="col-md-5">
              <img :src="newss.urlToImage" class="card-img" alt="..." />
            </div>
            <div class="col-md-7">
              <div class="card-body">
                <h5 class="card-title">{{newss.title}}</h5>
                <p class="card-text">
                  {{newss.description}}
                </p>
                <p class="card-text">
                  <small class="text-muted">Last updated 3 mins ago</small>
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "SectionApi",
  data() {
    return {
      news: null,
    };
  },
  mounted() {
    axios
      .get('http://newsapi.org/v2/top-headlines?country=us&category=business&apiKey=d1b3a702a4064218b65c13641fa04e55')
      .then((response) => {
        this.news = response.data.articles.slice(0,4);
        console.log(this.news);
      });
  },
};
</script>


<style scoped>
</style>