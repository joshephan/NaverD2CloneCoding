<template>
  <main>
    <Herobanner />
    <div class="home-layout">
      <div class="left-side">
        <Article v-for="item in articles" :item="item" :key="item.id" />
        <Article v-for="item in news" :item="item" :key="item.id" />
      </div>
      <div class="right-side">
        <Rankbox :items="rankList" />
        <Keywordbox />
        <Emailbox />
      </div>
    </div>
  </main>
</template>
<script>
import Herobanner from '~/components/Herobanner'
import Article from '@/components/card/Article';
import articleList from "../assets/data/article.json";
import newsList from "../assets/data/news.json";
import Rankbox from '@/components/Rankbox';
import Keywordbox from '@/components/Keywordbox';
import Emailbox from '@/components/Emailbox';

import _ from 'lodash';

export default {
  name: 'HomePage',
  components: {
    Herobanner,
    Article,
    Rankbox,
    Keywordbox,
    Emailbox
  },
  computed: {
    articles() {
      return articleList.list;
    },
    news() {
      return newsList.list;
    },
    rankList() {
      let array = _.concat(this.articles, this.news);      
      array = _.sortBy(array, ['viewCount']).reverse().splice(0,5);
      return _.map(array, 'title');
    }
  }
}
</script>
<style scoped>
.home-layout {
  max-width: 1180px;
  margin: auto;
  display: flex;
}
.left-side {
  max-width: 840px;
}
.right-side {
  margin-left: 60px;
  max-width: 250px;
}
</style>