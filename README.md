
[图片]
[图片]
### 1、两者的共同点是：不兼容低版本IE。
2、
[图片]
 ### 3、一个简单的vue程序：
[图片]
var s=new Vue({//模块里边放的内容
el:"选择器模块",
data:{//数据}，
methods:{//放方法其实就是函数。绑定事件的时候写处理函数：
show:funciton(){alert("ahah ")};
}
})
定义一个C变量来存储整个vue模块的内容：
el--相当于Element,s是固定的简写：”里边放的是对应下边的选择器“；
//里边放的是选择器（ 放I，class，便签名称都可以）
data：放的是我们的数据，要显示到用户页面中的数据。其实就是属性。
在下边要用{{}}来将使用从而显示。
data:{
msg:"可以是number，string，Boolean，Array，json, "
数组形式：arr:["1"，“2”，“3”],
json形式：arr1:{ name:"tom",age:"20",sex:39},
}
4、vue中常用的指令：
指令：就是扩展HTML便签的功能：扩展属性，方便使用。 
5、angular中常用的指令：
ng-model //定义模块
 ng-controller//定义控制器
ng-repeat//循环遍历
ng-click 事件
ng-show控制显示隐藏
 -----------------------------------------------------------
1.v-model;实现一个双向数据绑定功能。
一般用于表单元素（input ）
<scritp>
var s=new Vue({
el:"div1",
date:{
msg:"hello vue!"
}
});
</script>
<div id="div1">
<input type="text" v-model="msg"/><br>
{{msg}}
</div>
//就会实现一个双向数据绑定的动能、、
也可以用量个input去实现：
<input type="text" v-model="msg"/>
<input type="text" v-model="msg"/>
2、v-for=“变量名 in 数组名”遍历循环一大堆数据的
里边自带了一个{{$index}}//遍历数组的索引值。
循环数组：
[图片]

[图片]
循环json：
json:{ name:"tom",age:"20",sex:39},
[图片]
可以这么去显示， 
$key:是属性值。（键值）；
[图片]
k就是属性名；
v就是属性值；
会显示：属性名：属性值 索引  属性名
3、事件  v-on来绑定事件
v-on：事件名="事件处理函数"；
 
[图片]

[图片]

 上下对应
例一：现在我们想要实现点击按钮的时候添加一个水果：
[图片]
基于MVC，MVVM，当数据更新的时候，模板会自动跟着更新。
例二：点击按钮的时候div消失。
4、显示隐藏：v-show 指令
v-show="true/false";true显示。false隐藏。
<div id="app">
	  <input type="button" value="点击" v-on:click="a=false">
	  <div style="width:100px;height:100px;background:#090;" v-show="a"></div>
	</div>
</body>
<script type="text/javascript" src="vue.js"></script>
<script type="text/javascript">
	var V=new Vue({
		el:"#app",
		data:{
			a:true
		},
	});
</script>

实例三：bootstrap依赖jQuery   (CSS框架跟jQueryMoblie用法是一样的，只需要我们给我们的标签去附上class属性就可以)+vue简易留言板（todolist）
 
事件:简写v-on:==@click=“事件处理函数”；
@click=""。
 
