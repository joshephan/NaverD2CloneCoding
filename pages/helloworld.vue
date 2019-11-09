<template>
  <main>
    <Colorbanner title="Hello world" text="NAVER 개발자들이 직접 정리한 실전 개발 경험과 지식이 담겨진 블로그" bgColor="#7e57cc" />
    <section class="list-cover">
      <Article :item="articles[current - 1]"/>
      <b-pagination
        :total="articles.length"
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
import articleList from "../assets/data/article.json";

export default {
  name: 'HomePage',
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
    articles() {
      return articleList.list;
    }
  }
}
</script>
