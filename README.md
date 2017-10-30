# web-
<body>
	<div class="main" id="main">
		<!-- 图片轮播 -->
		<div class="banner" id="banners">
			<a href="">
				<div class="banner-slide slide1 slide-active"></div>
			</a>
			<a href="">
				<div class="banner-slide slide2"></div>
			</a>
			<a href="">
				<div class="banner-slide slide3"></div>
			</a>	 	
		</div>
		<!-- 上一张 下一张 -->
		<a href="javascript:void(0)" class="button prev"></a>
		<a href="javascript:void(0)" class="button next"></a>
		<!-- 圆点导航 -->
		<div class="dots">
			<span class="active"></span>
			<span></span>
			<span></span>
		</div>
	</div>
	<script src="js/script.js"></script>
</body>

// 封装一个代替getElemnetById的方法
function byId(id){
	return typeof(id) === "string"? document.getElementById(id):id;
}

var index = 0,
	timer = null,
	pics=byId("banners").getElementsByTagName('div'),
	len=pics.length;
	console.log(len);

function slideImg(){
	var main=byId("main");
	// 滑过清除定时器 离开继续
	
	main.onmouseover=function(){
	//滑过清除定时器 
	}
	main.onmouseout=function(){
		timer=setInterval(function(){
			index++;
			if(index>=3){
				index=0;
			}
			console.log(index);
		},2000);
	}
}

slideImg();
