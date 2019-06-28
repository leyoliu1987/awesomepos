/* eslint-disable */
<template>
  <div class="pos">
    <el-row>
      <el-col :span="7" class="pos-order" id="order-list">
        <el-tabs>
          <el-tab-pane label="点餐">
            <el-table :data="tableData" border style="width:100%">
              <el-table-column prop="goodsName" label="商品名称"></el-table-column>
              <el-table-column prop="count" label="数量" width="50"></el-table-column>
              <el-table-column prop="price" label="金额" width="70"></el-table-column>
              <el-table-column label="操作" width="100" fixed="right">
                <template>
                  <el-button type="text" size="small">删除</el-button>
                  <el-button type="text" size="small">增加</el-button>
                </template>
              </el-table-column>
            </el-table>
            <div class="div-btn">
              <el-button type="warning">挂单</el-button>
              <el-button type="danger">删除</el-button>
              <el-button type="success">结账</el-button>
            </div>
          </el-tab-pane>
          <el-tab-pane label="挂单">挂单</el-tab-pane>
          <el-tab-pane label="外卖">外卖</el-tab-pane>
        </el-tabs>
      </el-col>
      <el-col :span="17" class>
        <div class="often-goods">
          <div class="title">常用商品</div>
          <div class="often-goods-list">
            <ul>
              <li v-for="goods in oftenGoods" :key="goods.goodsId">
                <span >{{goods.goodsName}}</span>
                <span class="o-price">￥{{goods.price}}元</span>
                <span></span>
              </li>
            </ul>
          </div>
        </div>

        <div class="goods-type">
          <el-tabs>
            <el-tab-pane label="汉堡">
              <div>
                <ul class="cookList">
                   <li v-for="type0Goods in type0Goods" :key="type0Goods.goodsId">
                      <span class="foodImg"><img :src="type0Goods.goodsImg" width="100%"></span>
                      <span class="foodName">{{type0Goods.goodsName}}</span>
                     <span class="foodPrice">￥{{type0Goods.price}}元</span>
                  </li>
                </ul>
              </div>
            </el-tab-pane>
            <el-tab-pane label="小食">
              小食
            </el-tab-pane>
            <el-tab-pane label="饮料">
              饮料
            </el-tab-pane>
            <el-tab-pane label="套餐">
              套餐
            </el-tab-pane>
          </el-tabs>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'pos',
  data () {
    return {
      tableData: [
        {
          goodsName: '可口可乐',
          price: 8,
          count: 1
        },
        {
          goodsName: '香辣鸡腿堡',
          price: 15,
          count: 1
        },
        {
          goodsName: '爱心薯条',
          price: 8,
          count: 1
        },
        {
          goodsName: '甜筒',
          price: 8,
          count: 1
        }
      ],
      oftenGoods: [
        {
          goodsId: 1,
          goodsName: '香辣鸡腿堡',
          price: 18
        },
        {
          goodsId: 2,
          goodsName: '田园鸡腿堡',
          price: 15
        },
        {
          goodsId: 3,
          goodsName: '和风汉堡',
          price: 15
        },
        {
          goodsId: 4,
          goodsName: '快乐全家桶',
          price: 80
        },
        {
          goodsId: 5,
          goodsName: '脆皮炸鸡腿',
          price: 10
        },
        {
          goodsId: 6,
          goodsName: '魔法鸡块',
          price: 20
        },
        {
          goodsId: 7,
          goodsName: '可乐大杯',
          price: 10
        },
        {
          goodsId: 8,
          goodsName: '雪顶咖啡',
          price: 18
        },
        {
          goodsId: 9,
          goodsName: '大块鸡米花',
          price: 15
        },
        {
          goodsId: 20,
          goodsName: '香脆鸡柳',
          price: 17
        }
      ],
      type0Goods: [
        {
          goodsId: 1,
          goodsImg: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=4258866706,1746465872&fm=202&mola=new&crop=v1',
          goodsName: '香辣鸡腿堡',
          price: 18
        },
        {
          goodsId: 2,
          goodsImg: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=4258866706,1746465872&fm=202&mola=new&crop=v1',
          goodsName: '田园鸡腿堡',
          price: 15
        },
        {
          goodsId: 3,
          goodsImg: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=4258866706,1746465872&fm=202&mola=new&crop=v1',
          goodsName: '和风汉堡',
          price: 15
        },
        {
          goodsId: 4,
          goodsImg: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=4258866706,1746465872&fm=202&mola=new&crop=v1',
          goodsName: '快乐全家桶',
          price: 80
        },
        {
          goodsId: 5,
          goodsImg: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=4258866706,1746465872&fm=202&mola=new&crop=v1',
          goodsName: '脆皮炸鸡腿',
          price: 10
        },
        {
          goodsId: 6,
          goodsImg: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=4258866706,1746465872&fm=202&mola=new&crop=v1',
          goodsName: '魔法鸡块',
          price: 20
        },
        {
          goodsId: 7,
          goodsImg: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=4258866706,1746465872&fm=202&mola=new&crop=v1',
          goodsName: '可乐大杯',
          price: 10
        },
        {
          goodsId: 8,
          goodsImg: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=4258866706,1746465872&fm=202&mola=new&crop=v1',
          goodsName: '雪顶咖啡',
          price: 18
        },
        {
          goodsId: 9,
          goodsImg: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=4258866706,1746465872&fm=202&mola=new&crop=v1',
          goodsName: '大块鸡米花',
          price: 15
        },
        {
          goodsId: 20,
          goodsImg: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=4258866706,1746465872&fm=202&mola=new&crop=v1',
          goodsName: '香脆鸡柳',
          price: 17
        }
      ]
    }
  },
  mounted: function () {
    var orderHeight = document.body.clientHeight
    document.getElementById('order-list').style.height = orderHeight + 'px'
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.pos-order {
  background-color: #f9fafc;
  border-right: 1px solid #c0ccda;
}
.div-btn{
  margin-top: 20px;
}
.title{
  height: 20px;
  border-bottom: 1px solid #d3dce6;
  background-color: #f9fafc;
  padding: 10px;
  text-align: left;
}
.often-goods-list ul li{
   list-style: none;
   float: left;
   border:1px solid #b2b5b9;
   padding: 10px;
   margin: 10px;
   background-color:  #b2b5b9;
}
.o-price{
  color: #f551da
}
.goods-type{
  clear: both;
}
.cookList li{
  list-style: none;
  width:23%;
  border:1px solid #E5E9F2;
  height: auot;
  overflow: hidden;
  background-color:#fff;
  padding: 2px;
  float:left;
  margin: 2px;
}
.cookList li span{
  display: block;
  float:left;
}
.foodImg{
  width: 40%;
}
.foodName{
  font-size: 18px;
  padding-left: 10px;
  color:brown;

}
.foodPrice{
  font-size: 16px;
  padding-left: 10px;
  padding-top:10px;
}
</style>
