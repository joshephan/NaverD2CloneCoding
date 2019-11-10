<template>
  <main>
    <Colorbanner title="About D2" text="D2가 개발자들과 함께 걸어온 길을 소개합니다." bgColor="#0090d7" />
    <Schedule />
    <Timeline />
  </main>
</template>

<script>
import Colorbanner from '@/components/Colorbanner';
import Schedule from '@/components/Schedule';
import Timeline from '@/components/Timeline';
export default {
  name: 'AboutPage',
  components: {
    Colorbanner,
    Schedule,
    Timeline
  }
}
</script>
