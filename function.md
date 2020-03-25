# 常用的函数
#### 判断小数点的位置
```js
function decimalPoint(num){
   var x = String(num).indexOf('.')+1;   //小数点的位置
   var y = String(num).length - x;  //小数的位数
   if(y > 0){
	alert('这个数是小数,有'+y+'位小数');
	return true;				    
   }else{
	return false;
   }
}		
```  
### 进制转换
```js
function into(num){
   //十进制转其他
   var two = num.toString(2);
   var eight = num.toString(8);
   var six = num.toString(16);
   //其他转十进制
   parseInt(x,2);//二进制转十进制
   parseInt(x,8);//八进制转十进制
   parseInt(x,16);//十六进制转十进制
}
```      
