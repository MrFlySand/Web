![image](https://github.com/MrFlySand/Web/assets/59566818/ecb2ed02-0f7d-4e2f-9a8b-115f3450c084)

```
<script>
export default{  
  data(){
    return{
      selectAllValue:1,
      priceSums:0,
      push:{
        name:null,
        price:null,
        count:null,
        prices:null,
      },
      list:[{
          checked:'false',
          name:'微信公众号',
          src:'https://mp.weixin.qq.com/mp/qrcode?scene=10000004&size=102&__biz=MzkzMjE5OTMwOA==&mid=2247487964&idx=1&sn=f7474b00c99bb7017530e4fbffd0c62d&send_time=',
          introduce:'扫码关注，和群友们一起交流学习',
          price:9999,
          count:2,
          prices:null,
      },
      {
          checked:'false',
          name:'QQ交流群',
          src:'data:image/png;base64,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',
          introduce:'',
          price:6666,
          count:1,
          prices:null,
      },
      { 
          checked:'false',
          name:'MacBookPro',
          src:'https://img10.360buyimg.com/n2/jfs/t1/203950/20/28591/140129/637ca996E10cf6f5c/bb31749afd714364.jpg',
          introduce:'',
          price:21488,
          count:1,
          prices:null,
      }],    
    }
  },
  computed:{
    // 计算总和
    priceSums:function(){
      var sum = 0;
      for(var i = 0; i != this.list.length; i++){
        if(this.list[i].checked == true){
          sum = sum + this.list[i].price * this.list[i].count;
        }   
      }
      return sum;
    }
  },
  methods:{
    //减少物品个数
    reduce:function(index){
      this.list[index].count = this.list[index].count - 1;
      if(this.list[index].count == -1){
        this.list.splice(index,1)
      }
    },
    // 增加物品个数
    add:function(index){
      console.log(index)
      this.list[index].count = this.list[index].count + 1;
      return "this.list[index].count";  
    },
    // 添加新元素在购物车中
    pushValue:function(){    
      console.log(this.push.name)
      if(this.push.name == undefined) return 0;  
      for(var i=0; i<this.list.length; i++){
        if(this.list[i].name == this.push.name){
          alert("你已勾选此产品");
          return 0;
        }
      }
      this.list.push(this.push);
      this.push = {name:'', price:null, count:null};
    },
    // 选中所有
    selectAll:function(){
      for(var i=0,j=0; i<this.list.length; i++){
        if(this.list[i].checked == true){
          if(i==j){
            for(var k=0; k<this.list.length; k++){
              this.list[k].checked = false;
            }
            this.selectAllValue = false;
            return 0;    
          }
          j++;
        }
        this.list[i].checked = true;
      }
      this.selectAllValue = true;
    },
    // 删除选中
    selectDel:function(){
      if(confirm("你确认要删除吗？","提示框 ")){
        for(var i=0; i<this.list.length; i++){
          if(this.list[i].checked == true){
            this.list.splice(i,1);
          }
        }
      }
    }
  }
}
</script>

<template>
  <table>
    <!-- 表头 -->
    <tr style="font-weight: 800;">
      <td>序号</td>
      <td>商品</td>
      <td>单价（元）</td>
      <td>数量</td>
      <td>金额（元）</td>
    </tr> 

    <!-- 商品表 -->
    <tr v-for="(value,index) in list">
      <td><input type="checkbox" v-model="value.checked"></td>
      <td>
        <img v-bind:src="value.src" alt="图片" id="commodityImg">
        <span>{{value.name}}</span>
        <span style="font-size: 0.8em; color: #919191;">{{value.introduce}}</span>  
      </td>
      <td style="color: #e00000;">￥{{ value.price }}</td>
      <td style="padding: 0 !important;">
        <button @click="reduce(index)">-</button>
        <input type="text" v-model="value.count">
        <button @click="add(index)">+</button>
      </td>
      <td style="color: #e00000;font-weight: 800;">￥{{value.price*value.count}}</td>
    </tr>

    <!-- 添加商品 -->
    <tr id="add">
      <td></td>
      <td><input type="text" v-model="push.name" placeholder="商品"></td>
      <td><input type="text" v-model="push.price" placeholder="价格"></td>
      <td><input type="text" v-model="push.count" placeholder="数量"></td>
      <td><button id="push" @click="pushValue">添加</button></td>
    </tr>

    <!-- 全选、删除、合计等操作 -->
    <tr>
      <td colspan="2">
        <div @click="selectAll" ><input type="checkbox" v-model="selectAllValue">全选</div>
        <div @click="selectDel" >&nbsp;&nbsp;删除</div>
      </td>
      <td colspan="3">
        合计：<p style="color: #e00000;font-weight: 800;padding: 0.6em 0em; display: contents;">￥{{priceSums}}</p></td> 
    </tr>
  </table>
</template>


<style>
*{
  padding: 0; margin: 0;
}
button{
  /* margin-bottom: 10px !important; */
  /* border:1px solid #ccc; */
  width: 100%;
  height:100%;
  margin:0;
  padding: 0;
  border-radius: 0px;
}
#commodityImg{
  border:1px solid #000;
  margin-right:10px;
}
table{
  border:none;
  border-block: 4px solid #ccc;
  writing-mode: horizontal-tb;
  font-size: 1rem;
}
tr>td{
  border:1px solid #fff;
  padding:15px 10px;margin: 0;
  height: 40px !important;
}
tr>td:nth-child(2){
  width: 400px;
}
tr>td:nth-child(2)>img{
  width: 100px;
  float: left;
  display: block;
}
tr>td:nth-child(2)>span{
  display: flex;
}
tr>td:nth-child(4)>button,tr>td:nth-child(4)>input{
  width: 60px;height: 30px;
  border: none;
}
tr:last-child>td>div{
  display: inline;
  float: left;
  margin:0;padding:0 !important;
}
tr{
  padding:10px 20px;
  /* display: table-row; */
  border-block-end:2px solid #ccc; 
  writing-mode: horizontal-tb;
}
#push{
  margin: 0px !important;
  width: 100%;
  display: block;
  border: none;
}
input{
  border: none;
  text-align: center;
}

#add{
  font-weight: 800 !important;

}
#add input{
  height: 100%;
  border:1px solid #ccc;
}
#add input:active{
  border:1px solid #ccc !important;
}
</style>

<!-- 练习链接https://blog.csdn.net/qq_41605893/article/details/109539660 -->
```
