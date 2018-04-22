<template>
   <div>
    <div class="title">热销推荐</div>
       <ul>
      <router-link
        tag="li"
        class="item border-bottom"
               v-for="item of list"
        :key="item.id"
        :to="'/detail/' + item.id"
      >
        <img class="item-img" :src="item.imgUrl" />
               <div class="item-info">
                   <p class="item-title">{{item.title}}</p>
                   <p class="item-desc">{{item.desc}}</p>
                   <button class="item-button">查看详情</button>
               </div>
      </router-link>
       </ul>
   </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
  // data () {
  //   return {
  //     recommendList: [{
  //       id: '01',
  //       imgUrl: 'https://imgs.qunarzz.com/p/tts9/1803/eb/ab21dece1058d502.jpg_160x160_8e23825b.jpg',
  //       title: '海洋世界游泳馆',
  //       desc: '【可选上门接】北京八达岭长城+十三陵定陵或颐和园纯玩一日游'
  //     }, {
  //       id: '02',
  //       imgUrl: 'https://imgs.qunarzz.com/p/tts9/1803/eb/ab21dece1058d502.jpg_160x160_8e23825b.jpg',
  //       title: '海洋世界游泳馆',
  //       desc: '【可选上门接】北京八达岭长城+十三陵定陵或颐和园纯玩一日游'
  //     }]
  //   }
  // }
}
</script>

<style scoped lang="stylus">
@import '~styles/mixins.styl';
.title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
.item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
        width: 1.7rem
        height: 1.7rem
        padding: .1rem
    .item-info
        flex: 1
        padding: .1rem
        min-width: 0
        .item-title
            line-height: .54rem
            font-size: .32rem
            ellipsis()
        .item-desc
            line-height: .4rem
            color: #ccc
            ellipsis()
        .item-button
            line-height: .44rem
            margin-top: .16rem
            background: #ff9300
            padding: 0 .2rem
            border-radius: .06rem
            color: #fff
</style>
