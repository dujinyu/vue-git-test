<template>
	<div>
		<!-- this is test vue -->
		<!-- <a href="https://www.baidu.com">百度</a> -->
		<div v-for="(item, index) in msg" style="display: inline-block; margin-left: 30px;">
			<input type="checkbox" id="city">
			<label for="city">{{ item }}</label>
		</div>
		
	</div>	
</template>

<script>
	export default {
		name: "Hello",
		data() {
			return {
				msg: ["北京", "南京", "武汉", "上海"]
			}
		}
	}
</script>

<style>
	a {
		text-decoration: none;
	}
</style>