<template lang="html">
  <Panel title="生活服务" :class="$style.panel">
    <section :class="$style.list">
      <div :class="$style.item" v-for="item in enters" :key="item.img">
        <router-link :to="{ name: item.href}">
          <img :src="item.img" :alt="item.title">
          <h4>{{item.title}}</h4>
        </router-link>
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
    return{
      enters: [{
        title: '旅游',
        href: 'home',
        img: '//img12.360buyimg.com/jrpmobile/jfs/t12799/50/704102454/5247/19eac80a/5a4f2622Nc4aca701.png?width=90&height=90'
      }, {
        title: '医美',
        href: 'home',
        img: '//img12.360buyimg.com/jrpmobile/jfs/t16033/196/1306232362/4705/4c678227/5a4f265bN66ef5ae8.png?width=90&height=90'
      }, {
        title: '房抵押',
        href: 'home',
        img: '//img12.360buyimg.com/jrpmobile/jfs/t13051/63/2559290659/4702/e4068917/5a4f2693N937f1905.png?width=88&height=88"'
      }, {
        title: '驾校',
        href: 'home',
        img: '//img12.360buyimg.com/jrpmobile/jfs/t15133/16/1440686097/5786/1b038e03/5a4f26bfN03ed1f66.png?width=90&height=90'
      }]
    }
  }
}
</script>

<style lang="scss" module>
  @import '../../css/element.scss';
  .panel{
    .list{
      @include list(row);
      background: #fff;
      padding-top: 20px;
      padding-bottom: 20px;
      justify-content: space-around;
      a{
        text-decoration: none;
      }
      .item{
        text-align: center;
        img{
          display: inline-block;
          width: 90px;
          height: 90px;
        }
        h4{
          font-size: 26px;
          margin-top: 12px;
          color: #666;
        }
      }
    }
  }
</style>
