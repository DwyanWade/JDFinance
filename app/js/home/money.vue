<template lang="html">
  <Panel title="理财精选" :class="$style.panel">
    <section :class="$style.content">
      <dl :class="$style.item" v-for="item in items" :key="item.title">
        <dt >{{item.title}}<span>{{item.sub}}</span></dt>
        <dd>{{item.rate}}</dd>
        <dd>{{item.text}}</dd>
      </dl>
    </section>
  </Panel>
</template>

<script>
import Panel from '../core/panel.vue';
export default {
  components: {
    Panel,
  },
  data(){
    return {
      items: [{
          title: '定期理财',
          sub: '理财首选',
          rate: '5.50%',
          text: '历史年化结算利率'
      }, {
          title: '固定理财',
          sub: '理财推荐',
          rate: '5.80%',
          text: '综合年化率'
      }, {
          title: '智基账户',
          sub: '组合投资',
          rate: '8%-10%',
          text: '止盈利率收益率'
      }, {
          title: '小白理财',
          sub: '超短期',
          rate: '5.00%',
          text: '7日年化收益率'
      }]
    }
  }
}
</script>

<style lang="scss" module>
  @import '../../css/element';
  .panel{
    @include panel;
    .content{
      @include flex(row);
      justify-content: space-around;
      box-sizing: border-box;
      &:after{
       content: " ";
       display: block;
       width: 100%;
       height: 0px;
       box-sizing: border-box;
       border-bottom: 1px solid #ddd;
       position: relative;
       top: -208px;
     }
      .item{
        box-sizing: border-box;
        position: relative;
        width: 50%;
        &:after{
          content: " ";
          width: 1px;
          height: 136px;
          display: block;
          position: absolute;
          top: 50%;
          right: 0;
          margin-top: -68px;
          border-right: 1px solid #ddd;
        }
        &:nth-child(2n){
          &:after{
            display: none;
          }
        }
        padding: 34px 16px;
        dt{
          font-size: 30px;
          line-height: 42px;
          color: #333;
          span{
            font-size: 22px;
            color: #ff5155;
            border: 1px solid #ff5155;
            padding: 0 8px;
            vertical-align: 1px;
            margin-left: 2px;
          }
        }
        dd{
          &:nth-child(2){
            font-weight: 700;
            font-size: 44px;
            height: 58px;
            line-height: 58px;
            color: #FF5155;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
          }
          &:nth-child(3){
            font-size: 24px;
            height: 34px;
            line-height: 34px;
            color: #999;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
          }
        }
      }
    }
  }
</style>
