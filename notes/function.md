# 常用的函数
### 一个个打印文字
```js
function onePrint(){
	var index=0;
	var word="要输出的文字";
	function type(){		
		document.getElementById("").innerHTML = word.substring(0,index++);
	}setInterval(type, 180);
}
```
### 悬浮球
```html
<div id="SuspendedBall" style="top: 100px;left: 0;">更多</div>
```
```css
 #SuspendedBall{
    width: 25px;
    height: 25px;
    position:fixed;
    background-color: rgba(0,0,0,0.5);
    border-radius:25px;
    text-align: center;
    font-size: 10px;
    color: #fff;
    line-height: 25px;      		    
    border-style: solid;
}        	
/*电脑是否显示*/
/*@media screen and (max-width: 800px) {
	    .SuspendedBall{
		display: none;
	    }
	}*/
```
```js
function SuspendedBallButt(){
	window.location.href='https://mrflysand.github.io/html/WebsiteAll.html';
}
(function(){ 
	var flag = 0; //标记是拖曳还是点击
	var oDiv = document.getElementById('SuspendedBall');
	var disX,moveX,L,T,starX,starY,starXEnd,starYEnd;        
	oDiv.addEventListener('touchstart',function(e){
	    flag = 0;
	    e.preventDefault();//阻止触摸时页面的滚动，缩放
	    disX = e.touches[0].clientX - this.offsetLeft;
	    disY = e.touches[0].clientY - this.offsetTop;
			//手指按下时的坐标
	    starX = e.touches[0].clientX;
	    starY = e.touches[0].clientY;            
	});
	oDiv.addEventListener('touchmove',function(e){
	    flag = 1;
	    L = e.touches[0].clientX - disX ;
	    T = e.touches[0].clientY - disY ;
			//移动时 当前位置与起始位置之间的差值
	    starXEnd = e.touches[0].clientX - starX;
	    starYEnd = e.touches[0].clientY - starY;
	    if(L<0){//限制拖拽的X范围，不能拖出屏幕
		L = 0;
	    }else if(L > document.documentElement.clientWidth - this.offsetWidth){
		L=document.documentElement.clientWidth - this.offsetWidth;
	    }
	    if(T<0){//限制拖拽的Y范围，不能拖出屏幕
		T=0;
	    }else if(T>document.documentElement.clientHeight - this.offsetHeight){
		T = document.documentElement.clientHeight - this.offsetHeight;
	    }
	    moveX = L + 'px';
	    moveY = T + 'px';
	    this.style.left = moveX;
	    this.style.top = moveY;                  
	});
	SuspendedBall.addEventListener('touchend',function(e){
	    if(flag === 0) {//点击
		window.location.href='https://mrflysand.github.io/html/WebsiteAll.html';
	    }            													
	});		
})()
```    
### 输出换行
* 可以指定多少个元素换行
```js
function print(arr,leng,row){//数组,长度,行数
	for (var i=0;i<leng;i++) {
		var label =i+1;
		if(i%row!=row-1||i==0)
			document.write(label+"、"+arr[i]+"&nbsp&nbsp&nbsp");
		else
			document.write(label+"、"+arr[i]+"<br>");	
	}           		
}
```
### 判断小数点的位置
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
   parseInt(num,2);//二进制转十进制
   parseInt(num,8);//八进制转十进制
   parseInt(num,16);//十六进制转十进制
   //n进制转m进制
   document.write(parseInt(num,n).toString(m)+"<br>");
   //ASCII码转文本
   document.write(String.fromCharCode(parseInt(num,10))+"<br>")
}
```      
