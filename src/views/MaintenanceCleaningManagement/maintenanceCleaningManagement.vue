<template>
  <div id="orderManage">
    <btn id="btn" @btnStattus="handleBtnStattus"></btn>
    <real-time id="realTime" v-if="btnStatus.showRealTimeStatus"></real-time>
    <statistics  v-if="btnStatus.showStatisticsStatus"></statistics>
    <query  v-if="btnStatus.showQueryStatus"></query>
  </div>
</template>

<script>
  /* eslint-disable */
  import btn from '@/components/BtnSelect/btn'
  import realTime from './realTime/realTime'
  import statistics from './statistics/statistics'
  import query from './query/query'

  export default {
    name: "order-manage",
    components: {
      btn,
      realTime,
      statistics,
      query
    },
    data () {
      return {
        btnStatus: {
          showRealTimeStatus: true,
          showStatisticsStatus: false,
          showQueryStatus: false,
        }
      }
    },
    mounted () {
      this.$nextTick( ()=> {

      })
    },
    computed: {

    },
    methods: {
      handleBtnStattus (btnStattus) {
        this.btnStatus = btnStattus
      }
    }
  }
</script>

<style scoped>
  #orderManage{
    box-sizing: border-box;
    position: relative;
    padding: 1.5%;
    overflow-x: hidden;
    width: 100%;
    /*height: 57.5rem;*/
    height: 55.65rem;
  }
  #btn{
    position: absolute;
    top: 5px;
    right: 3%;
  }
  #realTime{
    box-sizing: border-box;
    background-color: #E9EEF1;
    margin-top: 2rem;
    width: 100%;
    height: 95%;
  }

</style>
