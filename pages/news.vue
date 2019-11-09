<template>
  <main>
    <Colorbanner title="D2 News" text="D2가 응원하는 개발자 행사 소식과 산출물들을 공유합니다." bgColor="#0ebb6b" />
    <section class="list-cover">
      <Article :item="news[current - 1]"/>
      <b-pagination
        :total="news.length"
        :current.sync="current"
        :simple="false"
        size="is-small"
        order="is-centered"
        :rounded="true"
        :per-page="1"
        :icon-prev="'chevron-left'"
        :icon-next="'chevron-right'">
      </b-pagination>
    </section>
  </main>
</template>

<script>
import Colorbanner from '@/components/Colorbanner';
import Article from '@/components/Article';
import newsList from "../assets/data/news.json";

export default {
  name: 'NewsPage',
  components: {
    Colorbanner,
    Article,
  },
  data() {
    return {
      current: 1
    }
  },
  computed: {
    news() {
      return newsList.list;
    }
  }
}
</script>
