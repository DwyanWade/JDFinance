<template lang="html">
  <Panel title="导航条" :class="$style.panel">
    <ul :class="$style.content">
      <li v-for="(item,index) in navLists">
        <router-link :to="{ name: item.path }">
          <img :src="item.img">
          <p>{{item.title}}</p>
        </router-link>
      </li>
    </ul>
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
      navLists: [
        {
          title: '首页',
          path: 'home',
          img: '//img12.360buyimg.com/jrpmobile/jfs/t3451/188/644771475/2428/800d7cb7/580f2435Nbfaa8055.png?width=66&height=66',
          selectImg: '//img12.360buyimg.com/jrpmobile/jfs/t3541/110/627394787/2190/5d02d39c/580f1dfdNcf72af31.png?width=66&height=66'
        },
        {
          title: '理财',
          path: 'money',
          img: '//img12.360buyimg.com/jrpmobile/jfs/t3811/55/345433999/2930/116d3dd1/580f1e25N028a1f2c.png?width=66&height=66',
          selectImg: '//img12.360buyimg.com/jrpmobile/jfs/t3559/44/615554467/2520/21aa9352/580f2400N4a7b5398.png?width=66&height=66'
        },
        {
          title: '白条',
          path: 'baitiao',
          img: '//img12.360buyimg.com/jrpmobile/jfs/t3343/179/621044750/1484/5af6b11a/580f50e4N005181d0.png?width=66&height=66',
          selectImg: '//img12.360buyimg.com/jrpmobile/jfs/t3673/27/676974575/1305/3f51b3c1/580f4e6eN6efa3e03.png?width=66&height=66'
        },
        {
          title: '我的',
          path: 'my',
          img: '//img12.360buyimg.com/jrpmobile/jfs/t3340/68/639059082/2591/800e2d6b/580f51cdN4caf20b2.png?width=66&height=66',
          selectImg: '//img12.360buyimg.com/jrpmobile/jfs/t3340/68/639059082/2591/800e2d6b/580f51cdN4caf20b2.png?width=66&height=66'
        }
      ]
    }
  },
}
</script>

<style lang="scss" module>
  @import '../../css/element.scss';
  .panel{
    @include panel;
    position: fixed;
    height: 100px;
    left: 0;
    right: 0;
    bottom: 0;
    margin: 0;
    z-index: 1;
    >h4{
      display: none;
    }
    .content{
      @include flex(row);
      justify-content: space-around;
      li{
        text-align: center;
        a{
          text-decoration: none;
        }
        img{
          height: 44px;
          width: 44px;
          display: inline-block;
          margin: 12px auto 6px;
        }
        p{
          color: #656565;
          font-size: 22px;
        }
        .router-link-active {
          color: #ff0000;
          font-size: 22px;
        }
      }
    }
  }
</style>
