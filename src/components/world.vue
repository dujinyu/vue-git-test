<template>
	<div>
		Hello world
		<br>
		<!-- 京东商品模板 -->
		<div ref="goodsSample" id="goodsSample" @mouseenter="enter" @mouseleave="leave">
			<!-- 商品展示图片——大图 -->
			<div class="p-img">
				<a target="_blank" href="https://item.jd.com/7694047.html" :title="adsAttach" id="b-img">
					<img :src="checkedImg" alt="">
				</a>
			</div>
			<!-- 商品多张图片——小图 -->
			<div class="s-img"  >
				<div id="haha" ref="haha" v-for="(item, index) in imgPath">
					<img :src="item" alt="" @mouseenter="addBorderColor(index, item)" @mouseleave="removeBorderColor(index)">
				</div>	
			</div>
			<div class="price">
					<span>￥ {{ price }}</span>
			</div>
			<div class="adsTotal">
				<a target="_blank" href="https://item.jd.com/7694001.html" :title="adsAttach">
					<span ref="adsItem" class="adsItem">{{ adsItem }}</span>
					<span class="adsAttach">{{ adsAttach }}</span>
				</a>
			</div>
			<div class="prodCommit">
				<span>
					<a id="commit-num" target="_blank" href="https://paipai.jd.com/pc/list.html?pid=7694047">{{ commitNum }}</a>
					条评论
				</span>
				<a id="ershou" target="_blank" href="https://paipai.jd.com/pc/list.html?pid=7694047">二手有售</a>
			</div>
			<div class="prod-shop">
				<span>
					<a href="https://mall.jd.com/index-1000000904.html" :title="prodShop">{{ prodShop }}</a>
					<a href="https://jdcs.jd.com/index.action?stock=%25EF%25BC%2588%25E6%259C%2589%25E8%25B4%25A7%25EF%25BC%2589&pid=7694047&score=5&evaluationRate=99&commentNum=%25E4%25BA%258C%25E6%2589%258B%25E6%259C%2589%25E5%2594%25AE&imgUrl=&wname=%25E8%258D%25A3%25E8%2580%25809i%25204GB+64GB%2520%25E5%25B9%25BB%25E5%25A4%259C%25E9%25BB%2591%2520%25E7%25A7%25BB%25E5%258A%25A8%25E8%2581%2594%25E9%2580%259A%25E7%2594%25B5%25E4%25BF%25A14G%25E5%2585%25A8%25E9%259D%25A2%25E5%25B1%258F%25E6%2589%258B%25E6%259C%25BA%2520%25E5%258F%258C%25E5%258D%25A1%25E5%258F%258C%25E5%25BE%2585&advertiseWord=%25E9%2599%2590%25E6%2597%25B6%25E4%25BC%2598%25E6%2583%25A01199%25EF%25BC%25811600%25E4%25B8%2587%25E5%2589%258D%25E7%25BD%25AE%25E6%2584%259F%25E5%2585%2589%25E5%25A2%259E%25E5%25BC%25BA%25E9%2595%259C%25E5%25A4%25B4%25EF%25BC%2581%25E8%258D%25A3%25E8%2580%2580%25E7%2588%2586%25E5%2593%2581%25E7%2589%25B9%25E6%2583%25A0%25EF%25BC%258C%25E9%2580%2589%25E5%2593%2581%25E8%25B4%25A8%25EF%25BC%258C%25E8%25B4%25AD%25E8%258D%25A3%25E8%2580%2580~&seller=%25E8%258D%25A3%25E8%2580%2580%25E4%25BA%25AC%25E4%25B8%259C%25E8%2587%25AA%25E8%2590%25A5%25E6%2597%2597%25E8%2588%25B0%25E5%25BA%2597&venderId=1000000904&entry=jd_search&" title="联系客服">
						<img src="https://img14.360buyimg.com/uba/jfs/t26764/156/1205787445/713/9f715eaa/5bc4255bN0776eea6.png" alt="">
					</a>
				</span>
			</div>
			<div class="jd">
				<span>自营</span>
			</div>
		</div>
	</div>	
</template>

<script>
	export default {
		name: "World",
		data() {
			return {
				imgPath: ["https://img12.360buyimg.com/n7/jfs/t21415/332/642302956/189613/778f2021/5b13cd6cN8e12d4aa.jpg", "https://img10.360buyimg.com/n7/jfs/t21532/360/764701806/223647/83d30500/5b1799cdN37efd6ec.jpg", "https://img11.360buyimg.com/n7/jfs/t19951/206/1198351272/188769/a0810744/5b17a8a1N2a25a442.jpg", "https://img14.360buyimg.com/n7/jfs/t20851/255/790931034/195488/954650a8/5b17aadbNcd580923.jpg"],
				checkedImg: "",
				price: 1199.00,
				ads: ["荣耀9i 4GB+64GB 幻夜黑 移动联通电信4G全面屏手机 双卡双待", "荣耀9i 4GB+64GB 魅海蓝 移动联通电信4G全面屏手机 双卡双待", "荣耀9i 4GB+64GB 梦幻紫 移动联通电信4G全面屏手机 双卡双待", "荣耀9i 4GB+64GB 碧玉青 移动联通电信4G全面屏手机 双卡双待"
				],
				adsItem: "",
				adsAttach: "限时优惠1199！1600万前置感光增强镜头！荣耀爆品特惠，选品质，购荣耀~",
				commitNum: 8000,
				prodShop: "荣耀京东自营旗舰店"
			}
		},
		methods: {
			enter() {
				//this.$refs.goodsSample.style.border = "1px solid #D5CCCC";
				this.$refs.goodsSample.style= "box-shadow: 2px 2px 2px #D5CCCC,2px -2px 2px #D5CCCC,-2px 2px 2px #D5CCCC,-2px -2px 2px #D5CCCC";
			},
			leave() {
				//this.$refs.goodsSample.style.border = "1px solid #FFFFFF";
				this.$refs.goodsSample.style= "box-shadow: ";
			},
			// checkedSmallPicture(src) {
			// 	this.checkedImg = src;
			// 	this.adsItem = this.ads[this.imgPath.indexOf(src)];
			// },
			addBorderColor: function(x, src) {
				this.$refs.haha[x].style.border = "2px solid red";
				this.checkedImg = src;
				this.adsItem = this.ads[this.imgPath.indexOf(src)];
				//this.message = "妈的";
				//this.$refs.littleImg.style.border = "2px solid red";
				// console.log(x)
			},
			removeBorderColor: function(x) {
				this.$refs.haha[x].style.border = "2px solid grey";
				//this.message = "去你妈的";
				//this.$refs.littleImg.style.border = "2px solid white";
				//console.log(x)
			}
		},
		created() {
			this.checkedImg = this.imgPath[0];
			this.adsItem = this.ads[0];
			this.$nextTick(() => {
				this.$refs.haha[0].style.border = "2px solid red";
				//大图片循环展示，小图片循环出现红色边框
				var interval = setInterval(() => {
					//var i = this.imgPath.indexOf(this.checkedImg) == -1 ? 0 : this.imgPath.indexOf(this.checkedImg);
					var i = this.imgPath.indexOf(this.checkedImg);
					this.$refs.haha[i].style.border = "2px solid grey";
					//console.log(i);
					if (i > this.imgPath.length - 2) {
						i = -1;
					};
					this.checkedImg= this.imgPath[i + 1];
						//console.log(this.$refs.haha[i]);
						//console.log(i);
					this.$refs.haha[i + 1].style.border = "2px solid red";
					
					this.adsItem = this.ads[i + 1];
					//console.log(this.checkedImg);
				}, 2000);
			});
			// 手机字样变为红色，功能有待实现
			// this.$nextTick(() => {
			// 	//console.log(this.$refs.goodsSample)
			// 	this.$refs.adsItem.innerHTML.
			// 	console.log(typeof this.$refs.adsItem.innerHTML)
			// })
			
		}
	}
</script>

<style>
	*{
		padding: 0px;
		margin: 0px;
	}
	#goodsSample {
		display: inline-block;
		width: 220px;
		padding: 12px 9px;
		/*overflow: hidden;*/
		/*border: 1px solid black;*/
	}
	#b-img {
		cursor: pointer;
		color: #666;
	}
	.s-img {
		height: 29px;
		text-align: left;
	}
	.s-img img {
		width: 25px;
		height: 25px;
		padding: 0px;
		margin: 0px;
		/*text-align: left;*/
		/*float: left;*/
		/*margin-left: 5px;*/
		/*margin-top: 2px;*/
	}
	#haha {
		display: inline-block;
		border: 2px solid grey;
		padding: 0px;
		margin: 0px;
		margin-right: 5px;
		height: 25px;
		/*line-height: 31px;*/
	}
	.price {
		/*position: relative;*/
		top: 10px;
		text-align: left;
		margin-top: 5px;
		margin-bottom: 8px;
		color: red;
		line-height: 22px;
		font-size: 20px;
		font-weight: 400;
		font-style: normal;
		font-family: Verdana;
		/*border: 1px solid black;*/
	}
	.adsTotal {
		line-height: 16px;
		overflow: hidden;
		font-size: 12px;
		text-overflow: clip;
		display: -webkit-box; 
		-webkit-box-orient: vertical;
		-webkit-line-clamp: 2; 
		/*padding-top: 10px;*/
		margin-bottom: 8px;
	}
	.adsTotal a:link {
		color: grey;
	}
	.adsTotal a:visited {
		color: grey;
	}
	.adsTotal a:hover {
		color: red;
	}
	.adsTotal a:active {
		color: grey;
	}
	.adsAttach {
		color: orange;
	}
	.prodCommit {
		display: flex;
		justify-content: space-between;
		font-size: 13px;
		margin-bottom: 15px;
		/*color: #9E8BF5;*/
	}
	.prodCommit span {
		color: grey;
	}
	#commit-num:link, #ershou:link {
		/*color: #9E8BF5;*/
		color: red;
	}
	#ershou:hover {
		color: red;
	}
	.prod-shop {
		margin-bottom: 10px;
	}
	.prod-shop span {
		display: flex;
		justify-content: flex-start;
	}
	.prod-shop span a:link {
		color: grey;
		font-size: 14px;
	}
	.prod-shop span a img {
		position: relative;
		left: 3px;
	}
	.jd span {
		float: left;
		display: inline-block;
		background-color: red;
		border-radius: 5px;
		color: white;
		font-size: 14px;
		height: 18px;
	}
</style>