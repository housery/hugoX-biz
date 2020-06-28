<template>
  <div class="home">
    <HelloWorld msg="手工介绍"/>
    <div class="good-list">
      <div class="goods" v-for="(goods, index) in items" :key="index">
        <h4 :title="goods.name">[{{goods.key + index}}] {{goods.name}}</h4>
        <div class="desc" :title="goods.desc"><p>{{goods.desc}}</p></div>
        <div class="img-box"><img class="goods-img" :src="goods.image" alt="花"></div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  },
  data(){
    return {
      items: [{
        key: "业务",
        name: "干花相框装饰",
        desc: "干花 Flower ['flauə] ，即利用干燥剂等使鲜花迅速脱水而制成的花。这种花可以较长时间保持鲜花原有的色泽和形态。我们平日摆放的鲜花许多都可以制成干花。",
        image: "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1568662751566&di=6463fc049099586636ee018afde38325&imgtype=0&src=http%3A%2F%2Fpic.51yuansu.com%2Fpic3%2Fcover%2F01%2F44%2F46%2F5939bad629de8_610.jpg"
      },{
        key: "业务",
        name: "干花相框装饰超好看",
        desc: "利用干燥剂等使鲜花迅速脱水而制成的花。这种花可以较长时间保持鲜花原有的色泽和形态。",
        image: "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1568662751566&di=ebfdff06e7c82a150aea2d1da674fc78&imgtype=0&src=http%3A%2F%2Fimg.11665.com%2Fimg03_p%2Fi3%2F12761024195643653%2FT1_ymmXA0eXXXXXXXX_%2521%25210-item_pic.jpg"
      }, {
        key: "业务",
        name: "干花相框装饰超好看",
        desc: "利用干燥剂等使鲜花迅速脱水而制成的花。这种花可以较长时间保持鲜花原有的色泽和形态。",
        image: "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1568662751563&di=5f2e2c6533163e7e33a83d040713960c&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201705%2F19%2F20170519053104_rJt4W.jpeg"
      }, {
        key: "业务",
        name: "干花相框装饰超好看",
        desc: "利用干燥剂等使鲜花迅速脱水而制成的花。这种花可以较长时间保持鲜花原有的色泽和形态。",
        image: "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1568662751560&di=c51ae7714843ac4daf9dbcdb83b1df65&imgtype=0&src=http%3A%2F%2Fbrup.shengri.cn%2Fgoods%2F2018%2F09%2FFm0jYQ8ngc2b2GMe5VKF-zEOzF3g.jpg"
      }, {
        key: "业务",
        name: "干花相框装饰超好看",
        desc: "利用干燥剂等使鲜花迅速脱水而制成的花。这种花可以较长时间保持鲜花原有的色泽和形态。",
        image: "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1568662751581&di=fb6641309fd7736e7300e4a49d97a7c2&imgtype=0&src=http%3A%2F%2Fimg010.hc360.cn%2Fhb%2FMTQ3MjA4OTcxMTU2Ni0xMzI4MjM2MTk4.jpg"
      },{
        key: "业务",
        name: "干花相框装饰",
        desc: "干花 Flower ['flauə] ，即利用干燥剂等使鲜花迅速脱水而制成的花。这种花可以较长时间保持鲜花原有的色泽和形态。我们平日摆放的鲜花许多都可以制成干花。",
        image: "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1568662751566&di=6463fc049099586636ee018afde38325&imgtype=0&src=http%3A%2F%2Fpic.51yuansu.com%2Fpic3%2Fcover%2F01%2F44%2F46%2F5939bad629de8_610.jpg"
      }]
    }
  }
}
</script>

<style scoped>
  .good-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start;
    align-items: start;
  }

  .goods {
      padding: 5px;
      width: 44vw;
  }

  .goods:hover {
      box-shadow: 2px 2px 10px #999;
  }

  .img-box {
    display: flex;
    justify-content: center;
  }

  .goods-img {
    width: 38vw;
  }

  h4, p {
    margin: 5px 10px;
  }
  h4 {
    font-size: 1em;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  p {
    font-size: .7em;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 3;
    overflow: hidden;
  }
</style>
