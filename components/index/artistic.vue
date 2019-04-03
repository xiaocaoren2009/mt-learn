<template>
  <section class="m-istyle">
    <dl @mouseover="mouseover">
      <dt>有格调</dt>
      <dd :class="{active:kind==='all'}" kind="all" keyword="景点">
        全部
      </dd>
      <dd>
        约会聚餐
      </dd>
      <dd>
        丽人SPA
      </dd>
      <dd>
        电影演出
      </dd>
      <dd>
        品质出游
      </dd>
    </dl>
    <ul class="ibody">
      <li v-for="item in list.all" :key="item.title">
        <el-card :body-style="{ padding: '0px' }" shadow="never" >
          <img :src="item.img" class="image">
          <ul class="cbody">
            <li class="title">{{ item.title }}</li>
            <li class="sub-title">{{ item.subtitle }}</li>
            <li class="price">¥<em>{{ item.price }}</em></li>
            <li class="pos">{{ item.pos }}</li>
          </ul>
        </el-card>
      </li>
    </ul>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        kind: "all",
        list: {
          all: [{
            title: '大董',
            subtitle: '糖醋黄鱼五四套餐',
            img: 'https://p0.meituan.net/msmerchant/f0f72ccd78773cc5a0156b1c00d588c0961404.jpg@736w_416h_1e_1c',
            price: '1296',
            pos: '王府井/东单'
            },{
            title: '元祖食品',
            subtitle: '蛋糕3选1，约10英寸',
            img: 'https://p0.meituan.net/msmerchant/99c455bf54275263f48f9592197a4864740268.jpg@736w_416h_1e_1c',
            price: '275',
            pos: '双井'
            },{
            title: '大董',
            subtitle: '糖醋黄鱼五四套餐',
            img: 'https://p0.meituan.net/msmerchant/f0f72ccd78773cc5a0156b1c00d588c0961404.jpg@736w_416h_1e_1c',
            price: '1296',
            pos: '王府井/东单'
            },{
            title: '元祖食品',
            subtitle: '蛋糕3选1，约10英寸',
            img: 'https://p0.meituan.net/msmerchant/99c455bf54275263f48f9592197a4864740268.jpg@736w_416h_1e_1c',
            price: '275',
            pos: '双井'
            },{
            title: '大董',
            subtitle: '糖醋黄鱼五四套餐',
            img: 'https://p0.meituan.net/msmerchant/f0f72ccd78773cc5a0156b1c00d588c0961404.jpg@736w_416h_1e_1c',
            price: '1296',
            pos: '王府井/东单'
            },{
            title: '元祖食品',
            subtitle: '蛋糕3选1，约10英寸',
            img: 'https://p0.meituan.net/msmerchant/99c455bf54275263f48f9592197a4864740268.jpg@736w_416h_1e_1c',
            price: '275',
            pos: '双井'
            }
          ],
          part: [],
          spa: [],
          movie: [],
          travel: []
       }
      };
    },
    computed: {
      cur: () => {
        return this.list[this.kind];
      }
    },
    methods: {
      mouseover() {

      }
    }
  }
</script>

<style scope lang="scss">
  @import "@/assets/css/index/artistic.scss";
</style>