<template>
	<div class="box">
		<header>
			<router-link tag="span" to="/">{{str}}</router-link>
			<input type="text" placeholder="大家正在搜索:****">
			<span class="btn">搜索</span>
		</header>
		<main>
			<p>热门搜索</p>
			<div class="list">
				<span v-for="(v,i) in data" :key="i">{{v}}</span>
			</div>
		</main>
	</div>
</template>

<script>
export default {
	data(){
		return {
			str:"<",
			data:["爆款","女式羽绒服","男生羽绒服"]
		}
	}
}
</script>
<style lang="scss" scoped>
*{
	margin: 0;
	padding: 0;
}
.box{
	width: 100%;
	height: 100%;
	header{
		width: 100%;
		height: 50px;
		border-bottom: 1px solid #ccc;
		display: flex;
		span{
			width: 15%;
			text-align: center;
			line-height: 50px;
			&:nth-child(1){
				font-size: 36px;
			}
		}
		input{
			width: 70%;
			height: 50%;
			margin-top: 9px;
		}
	}
	main{
		flex:1;
		p{
			margin: 8px;
		}
		span{
			border: 1px #ccc solid;
			padding: 3px;
			margin: 5px;
		}
	}
}
</style>