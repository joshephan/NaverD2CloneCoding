<template>
  <main>
    <Colorbanner title="D2 Program" text="가치 있는 기술 지식 생산을 돕고, 경험을 나누며, 개발자를 지원합니다." bgColor="#00b485" />
    <section class="list-cover">
      <Program v-for="p in programs" :program="p" :key="p.title" />
    </section>
  </main>
</template>

<script>
import Colorbanner from '@/components/Colorbanner';
import Program from '@/components/Program';
import programList from "../assets/data/program.json";

export default {
  name: 'ProgramPage',
  components: {
    Colorbanner,
    Program
  },
  computed: {
    programs() {
      return programList.list;
    }
  }
}
</script>
