<template>
  <div>
    <Chart :cdata="cdata" />
  </div>
</template>

<script>
import Chart from './chart.vue';
export default {
  data () {
    return {
      cdata: {
        xData: ["rose1", "rose2", "rose3", "rose4",],
        seriesData: [
          { value: 10, name: "厨余垃圾" },
          { value: 5, name: "可回收垃圾" },
          { value: 15, name: "有害垃圾" },
          { value: 25, name: "其他垃圾" },
        ]
      }
    }
  },
  components: {
    Chart,
  },
  mounted () {
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>
</style>