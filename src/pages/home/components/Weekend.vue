<template>
   <div>
    <div class="title">周末去哪儿</div>
       <ul>
           <li class="item border-bottom"
               v-for="item of list"
               :key="item.id">
               <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
               </div>
               <div class="item-info">
                   <p class="item-title">{{item.title}}</p>
                   <p class="item-desc">{{item.desc}}</p>
               </div>
           </li>
       </ul>
   </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
  // data () {
  //   return {
  //     recommendList: [{
  //       id: '01',
  //       imgUrl: 'https://ugc.qunarzz.com/2/88973e3.png_r_1500x_afe2715f.png',
  //       title: '海洋世界游泳馆',
  //       desc: '【可选上门接】北京八达岭长城+十三陵定陵或颐和园纯玩一日游'
  //     }, {
  //       id: '02',
  //       imgUrl: 'https://ugc.qunarzz.com/2/d1373f47.jpg_r_1500x_053b0e6c.jpg',
  //       title: '海洋世界游泳馆',
  //       desc: '【可选上门接】北京八达岭长城+十三陵定陵或颐和园纯玩一日游'
  //     }]
  //   }
  // }
}
</script>

<style scoped lang="stylus">
    @import '~styles/mixins.styl'
    .title
        line-height: .8rem
        background: #eee
        text-indent: .2rem
    .item-img-wrapper
        overflow: hidden
        height: 0
        padding-bottom: 37.09%
        .item-img
            width: 100%
    .item-info
        padding: .1rem
        .item-title
            line-height: .54rem
            font-size: .32rem
            ellipsis()
        .item-desc
            line-height: .4rem
            color: #ccc
            ellipsis()
</style>
