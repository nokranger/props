<template>
  <div>
    <blog-post v-for="(testss, index) in test" :key="index" :titles="testss.title"></blog-post>
    <blog-post titles="Props"></blog-post>
    <blog-post titles="test"></blog-post>
    <blog-post titles="Prosp" bgColor="black" :height="200" color="white" url="https://www.youtube.com/watch?v=W2j7CjQI2y2"></blog-post>
  </div>
</template>
<script>
import propss from '../views/props'
export default {
  components: {
    'blog-post': propss
  },
  data () {
    return {
      test: [
        { id: '1', title: 'fsafasfasfa' },
        { id: '2', title: 'fasfasfasasf33rf3r3' },
        { id: '3', title: 'xcbcxbxbxcbxb' }
      ],
      cssProps: {
        'background-color': 'white',
        height: '200px',
        color: 'black'
      }
    }
  },
  computed: {
  }
}
</script>
<style>
</style>
