<template>
  <div>
    <h3 :style="btnStyles">{{titles}}</h3>
    <button>AAAA</button>
    {{test}}
    <video width="400" controls>
      <source :src="url" type="video/mp4">
      <source :src="url" type="video/ogg">
      not support
    </video>
    <!-- <blog-post title="test eiei"></blog-post> -->
  </div>
</template>
<script>
export default {
  props: {
    titles: {
      type: String,
      required: true,
      default: 'This is default'
    },
    bgColor: {
      type: String,
      default: '#0099CC'
    },
    height: {
      type: Number,
      default: 100
    },
    color: {
      type: String,
      default: 'red'
    },
    url: {
      type: String,
      default: 'https://www.youtube.com/watch?v=W2j7CjQI2y4'
    }
  },
  mounted () {
  },
  computed: {
    btnStyles () {
      return {
        'background-color': this.bgColor,
        height: `${this.height}px`,
        color: this.color
      }
    },
    test () {
      return console.log(this.url)
    }
  }
}
</script>
<style>
</style>
