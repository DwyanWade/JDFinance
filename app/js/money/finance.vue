<template lang="html">
  <Panel title="理财精选" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.item" v-for="item in items">
        <img :src="item.img" alt="">
        <div>
          <span>{{item.title}}</span>
          <span>{{item.description}}</span>
        </div>
        <em>去赚钱 > </em>
      </div>
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
      items: [
        {
          title: '月度理财',
          description: '预期年化收益率4.50%',
          img: '//img12.360buyimg.com/jrpmobile/jfs/t3670/58/543125556/2606/a65096b9/580d80afN63b1085a.png?width=76&height=76'
        },
        {
          title: '季度理财',
          description: '历史年化回报率5.50%',
          img: '//img12.360buyimg.com/jrpmobile/jfs/t3679/44/511862277/2728/c1c6b2bf/580d8189N6b6f8052.png?width=76&height=76'
        },
        {
          title: '一年理财',
          description: '历史年化回报率5.80%',
          img: '//img12.360buyimg.com/jrpmobile/jfs/t3331/69/580199498/3074/d5bb21c5/580d7f6cN7f35e596.png?width=76&height=76'
        }
      ]
    }
  }
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';
@import '../../css/layout.scss';
.panel{
  @include panel;
  >h4{
    border-bottom: 1px solid #ddd;
  }
  .content{
    .item{
      @include flex(row);
      align-items: center;
      height: 140px;
      &:after{
        content: " ";
        box-sizing: border-box;
        border-bottom: 1px solid #ddd;
        width: 100%;
        height: 0;
        margin-left: 150px;
        margin-top: 30px;
      }
      &:last-child:after{
        border-color: #fff;
      }
      img{
        width: 88px;
        height: 88px;
        line-height: 88px;
        display: inline-block;
        margin: 24px 32px 0;
      }
      >div{
        height: 88px;
        width: 334px;
        margin: 26px 0 0;
        span:first-child{
          font-size: 32px;
          color: #333;
        }
        span:last-child{
          font-size: 24px;
          line-height: 1.1;
          color: #ff3232;
          overflow: hidden;
          white-space: nowrap;
          text-overflow: ellipsis;
        }
      }
      >em{
        font-size: 28px;
        color: #FF801A;
      }
    }
  }
}
</style>
