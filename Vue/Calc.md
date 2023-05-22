![image](https://github.com/MrFlySand/Web/assets/59566818/cb890263-aaab-4598-8982-18326746980e)

```vue
<script>
export default{
    data(){
        return{
            sumValue:"0",
            arr:[["x<sup>2</sup>","1/x","C","✖"],[7,8,9,"/"],[4,5,6,"*"],[1,2,3,"-"],[".",0,"=","+"]]        
        };
    },
    methods:{
        getSum:function(index,i){
            console.log(index+":"+i)
            if(index==0 && i==0){
                console.log(Math.pow(this.sumValue,2));
                this.sumValue = Math.pow(this.sumValue,2);
            }else if(index==0 && i==1){
                console.log(this.sumValue)
                this.sumValue = 1.0/this.sumValue;                    
            }else if(index==0 && i==2){
                this.sumValue = 0;                    
            }else if(index==0 && i==3){        
                this.sumValue = this.sumValue.substring(0, this.sumValue.length - 1);;                    
            }else if(index==4 && i==2){
                this.sumValue = "结果："+eval(this.sumValue);            
            }else if(this.sumValue == '0' || this.sumValue[0]=="结"){
                this.sumValue = this.arr[index][i].toString();
            }else if(this.sumValue != '0' && this.arr[index][i].toString()!="="){                
                this.sumValue = this.sumValue + this.arr[index][i].toString();
            }            
        },
    }
}
</script>
<template>
    <table>
        <tr>
            <td colspan="4" style="padding: 0">
                <input type="text" v-model="sumValue">
            </td>
        </tr>
        <tr v-for="(value,index) in arr" :key="value">
            <td  v-for="(val,i) in value" :key="val" @click="getSum(index,i)"  @keyup.enter="print(index,i)" v-html="val"></td>
        </tr>        
    </table>
    <p style="color: red;">微信公众号：小知识酷，关注获取更多</p>
</template>
<style>
*{
    padding: 0;margin: 0;
}
table{
    /* border: 2px solid #000; */
    user-select: none;
    background-color: #eeeeee;
}
table td{
    /* border: 1px solid #000; */
    padding: 3px 16px;
    background: #fff;
}
table td:hover{
    background-color: #eee;
}
table td:active{
    background-color: #ddd;
    
}
table tr:nth-child(1) td:hover{
    background-color: #fff;
}
input{
    border: none;
    padding-top: -10px;
    text-align: right;
    outline: none;

}
</style>
```
