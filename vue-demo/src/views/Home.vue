<template>
  <div class="home">
    <div class="header">
      <div>登陆</div>
      <div class="inp" @click="btnClick('/about')">大家在搜</div>
      <div @click="btnClick('/classify')">分类</div>
      <!-- <button @click="btnClick('/about')">搜索</button>
      <button @click="btnClick('/classify')">分类</button>
      <button @click="btnClick('/list')">详情</button> -->
    </div>
    <div class="con">
      <div class="nav" @click="btnClick('/list')">
        <ul class="NavList">
          <li v-for="(item,key) in list" :key="key" class="item">
            {{item.title}}
          </li>
        </ul>
      </div>
      <div class="banner"></div>
      <div class="warp">
        <dl v-for="(item,key) in warp" :key="key">
          <dt></dt>
          <dd>{{item.title}}</dd>
        </dl>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:'',
  data () {
    return {
      list:[
        {title:'今日推荐'},
        {title:'最后疯抢'},
        {title:'美妆'},
        {title:'母婴'},
        {title:'国际'},
        {title:'家电'},
        {title:'童鞋'},
        {title:'男装'}
      ],
      warp:[
        {title:'女装'},
        {title:'男装'},
        {title:'鞋包'},
        {title:'内衣'},
        {title:'保暖管'},
        {title:'户外运动'},
        {title:'母婴童装'},
        {title:'美妆护肤'},
        {title:'手表配饰'},
        {title:'清仓'}
      ]
    };
  },

//   components: {},

//   computed: {},

//   mounted: {},
// //方法
  methods: {
    btnClick(path){
      this.$router.push({
        path:path
      })
    }
  }
}

</script>
<style lang='scss' scoped>
html,body{
  width: 100%;
  height: 100%;
}
.home{
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.header{
  width: 100%;
  height: 40px;
  display: flex;
  text-align: center;
  div{
    width: 60px;
    height: 40px;

  }
  .inp{
    flex:1;

  }
}

.NavList{
  width: 100%;
  height: 40px;
  display: flex;
  // flex-wrap: wrap;
  overflow: auto;
  .item{
    flex-shrink: 0;
    width: 100px;
    height: 40px;
    text-align: center;
    line-height: 40px;
  }
}
.banner{
  width: 100%;
  height: 200px;
  background: #ccc;
}
.warp{
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  font-size: 16px;
  text-align: center;
  margin-top: 5px;
  dl{
    width: 20%;
    dt{
      width: 40px;
      height: 40px;
      background: #ccc;
      margin: 0 auto;
    }
  }
}
</style>