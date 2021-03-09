<template>
  <div>
    <Chart :cdata="cdata" />
  </div>
</template>

<script>
import Chart from './chart.vue'
export default {
  data () {
    return {
      cdata: {
        category: [
          "1月",
          "2月",
          "3月",
          "4月",
          "5月",
          "6月",
          "7月",
        ],
        lineData: [
          18,
          20,
          24,
          28,
          56,
          62,
          59,
        ],
        barData: [
          46,
          50,
          55,
          225,
          140,
          210,
          85,
        ],
        rateData: []
      }
    };
  },
  components: {
    Chart,
  },
  mounted () {
    this.setData();
  },
  methods: {
    // 根据自己的业务情况修改
    setData () {
      for (let i = 0; i < this.cdata.barData.length -1; i++) {
        let rate = this.cdata.barData[i] / this.cdata.lineData[i];
        this.cdata.rateData.push(rate.toFixed(2));
      }
    },
  }
};
</script>

<style lang="scss" scoped>
</style>